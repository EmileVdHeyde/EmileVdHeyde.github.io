## Web Scraping Data from a Json page to Datafame 

**Project description:** 

This project uses an Free API and extract a selection of data points relating to the countries of the world.
This is a excercise in getting the data into a dataframe sructure , wrangeling some data issues and over coming the sometimes multiple responses per targetd column

[Click here to View .py or .ipynb files relating to this project] (https://github.com/EmileVdHeyde/My-Python-Projects/tree/master/1.Covid%20Data%20Web%20Scraping)

[Click here to View .py or .ipynb files relating to this project](http://github.com/EmileVdHeyde/My-Python-Projects/tree/master/1.Covid%20Data%20Web%20Scraping)

### 1. Suggest hypotheses about the causes of observed phenomena

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

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

### 2. Assess assumptions on which statistical inference will be based

```javascript
if (isAwesome){
  return true
}
```

### 3. Support the selection of appropriate statistical tools and techniques

<img src="images/dummy_thumbnail.jpg?raw=true"/>

### 4. Provide a basis for further data collection through surveys or experiments

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
