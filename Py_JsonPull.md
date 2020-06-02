## Web Scraping Data from a Json page to Dataframe 

[Back to Project List](http://emilevdheyde.github.io/)

**Project description:** 

This project uses an Free API and extract a selection of data points relating to the countries of the world.
This is a excercise in getting the data into a dataframe sructure , wrangeling some data issues and over coming the sometimes multiple responses per targeted column as well as inforcing error control. 

[Click here to View .py or .ipynb files relating to this project](https://github.com/EmileVdHeyde/My-Python-Projects/tree/master/3.JSON%20API)

### 1. Build a function genrates a list of county names

Pulling from the Json stored data , we extract the first element the country name and build a list. 
This is important for the user to specify the countries they want , or to select all countries in the next steps. 

```python
def list_of_countries(number_to_return=300):

    allurl='https://restcountries.eu/rest/v2/all'

    uh=urllib.request.urlopen(allurl)
    data = uh.read().decode()
    z=json.loads(data)
    
    lim=number_to_return 
    country_list=list()
    
    i=0
    while i < lim :
        y=z[i]
        country_list.append(y['name'])
        i+=1 
        
    return  country_list
```

### 2. Define a function to pull a list of page links 

Build a list of each countries web page that we will extract from 

```python
def get_country_data_links(country):
   # country_name=country       #needs to be more sensitive to specia chars and blanks
    country_name=country ##.replace(" ", "%20")
   #country_name=urllib.parse.unquote(country, encoding='utf-8', errors='replace')
    url = (serviceurl + quote(country_name))
    print(url)
```

### 3. Define a function that pulls all the data from a Json file 

Loop through the links , extract data , error control and handle blank fields

```python
def get_country_data(country):
   # country_name=country       #needs to be more sensitive to specia chars and blanks
    country_name=country ##.replace(" ", "%20")
   #country_name=urllib.parse.unquote(country, encoding='utf-8', errors='replace')
    url = serviceurl + quote(country_name)
    try: 
        uh = urllib.request.urlopen(url)
    except HTTPError as e:
        print("Sorry! Could not retrive anything")
        return None
    except URLError as e:
        print('Failed to reach a server.')
        print('Reason: ', e.reason)
        return None
    else:
        data = uh.read().decode()
        data=data.replace('[]',"[0,0]")
        print("Retrieved data on {}. Total {} characters read.".format(country_name,len(data)))
        return data
```

### 4. Define a function to stucture and store a the data in a predifined structure 

Extract and shape data following the JSON structure to build a dictionary
Fix special character and space issues
Handle errors with blank data and indexing issues

```python
def build_country_database(list_country):
    """
    """
    # Define an empty dictionary with keys
    country_dict={'Country':[],'Capital':[],'Region':[],'Sub-region':[],'Population':[],
                  'Lattitude':[],'Longitude':[],'Area':[],'Gini':[],'Timezones':[],
                  'Currencies':[],'Languages':[]}
    
    for c in list_country:
        data = get_country_data(c)
        if data!=None:
            x = json.loads(data)
            y=x[0]
            country_dict['Country'].append(y['name'])
            country_dict['Capital'].append(y['capital'])
            country_dict['Region'].append(y['region'])
            country_dict['Sub-region'].append(y['subregion'])
            country_dict['Population'].append(y['population'])
            country_dict['Lattitude'].append(y['latlng'][0])
            country_dict['Longitude'].append(y['latlng'][1])
            country_dict['Area'].append(y['area'])
            country_dict['Gini'].append(y['gini'])
            # Note the code to handle possibility of multiple timezones as a list
            if len(y['timezones'])>1:
                country_dict['Timezones'].append(','.join(y['timezones']))
            else:
                country_dict['Timezones'].append(y['timezones'][0])
            # Note the code to handle possibility of multiple currencies as dictionaries
            if len(y['currencies'])>1:
                lst_currencies = []
                for i in y['currencies']:
                    if i['name'] != None :
                        lst_currencies.append(i['name'])
                country_dict['Currencies'].append(','.join(lst_currencies))
            else:
                country_dict['Currencies'].append(y['currencies'][0]['name'])
            # Note the code to handle possibility of multiple languages as dictionaries
            if len(y['languages'])>1:
                lst_languages = []
                for i in y['languages']:
                    lst_languages.append(i['name'])
                country_dict['Languages'].append(','.join(lst_languages))
            else:
                country_dict['Languages'].append(y['languages'][0]['name'])
    
    # Return as a Pandas DataFrame
    return pd.DataFrame(country_dict)
```

### 5. Use the functions to make it easy for the user to retrive the data for a specific country

Allow entry of a country name into function to return information


This code is a code improvement of the base code from 
[link](https://github.com/tirthajyoti/Web-Database-Analytics/blob/master/Countries-JSON-API.ipynb)

Improvements included ; 

-Fixing the original code to work with all countries and not just a selection

-There was issues relating to special characters and multi word country names not loading

-The json file contain some nones which caused indexing errors 

-There was no mechanism to look up country names.


**Packages Used: 
URLIB | JSON | PANDAS

[Back to Project List](http://emilevdheyde.github.io/)
