# SDV601 - Week 11 Blog

------

#### <u>Connecting to an http (JSON) API</u>

------

What have I learned?

This week I learned about sending data to and from JSNDrop with different URL strings. Like the name suggests, the data that is sent and is received is in a JSON format. This is a simple and useful way to store data in a remote storage from anywhere.

Below is some examples of the different methods we can use:

**CREATE** - Creates a table

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"CREATE":"tblTest","EXAMPLE":{"PersonID PK":"Todd","Score":21}}}`

**STORE** - Stores data in a table

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"STORE":"tblTest","VALUE":[{"PersonID":"Todd","Score":21},{"PersonID":"Jane","Score":2000}]}}`

**ALL** - Selects all data from the table

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"ALL":"tblTest"}} `

**SELECT** - Selects data based on a clause

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"SELECT":"tblTest","WHERE":"Score > 200"}}`

**DELETE** - Deletes data from a table based on a clause

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"DELETE":"tblTest","WHERE":"PersonID = 'Jane'"}}`

**DROP** - Drops the table from the database

`https://newsimland.com/~todd/JSON/?tok={"tok":"Y O U R T O K E N GOES HERE","cmd":{"DROP":"tblTest"}}`

## Assessment ~ 

I managed to implement it into python so that I could pass a JSON object to the database as well as pull the data from the table. Below is how I did this:

**STORE**

```python
def UploadData(root, self, data):
	json_data = data.to_json(orient='records')[1:-1] # Converts the data to JSON
	url = 'https://newsimland.com/~todd/JSON/?tok={"tok":"fc82391c-71b3-4134-91b2-6a40f6b28a94","cmd":{"STORE":"sdv_data_daniel","VALUE":			['+ str(json_data) +']}}' # Defines the URL that we will pass with the json_data as the "VALUE"
    r = requests.get(url) # Uses the get method passing the url as a paramater
```

**ALL**

```python
    def RetireveData(self):
        url = 'https://newsimland.com/~todd/JSON/?tok={"tok":"fc82391c-71b3-4134-91b2-6a40f6b28a94","cmd":{"ALL":"sdv_data_daniel"}}'
        r = requests.get(url) # Request Data From Url
        data = r.json() # Defines data as the respons
        data = json.dumps(data['Msg']) # Convert data to JSON object
        df = pd.read_json(data)# Convert json to dataframe
```


------

How have I learned this?

I have learned this by following the steps provided to us on Moodle and testing if it works


------

Why have I learned this?

- A simple way of storing data in a remote database
- An alternative to options such as MySQL, Firebase, and MongoDB
- Will be useful for future tasks such as milestone three


------

What will I do to remember this learning?

- I will practice using this method
- Try and implement it into my code
