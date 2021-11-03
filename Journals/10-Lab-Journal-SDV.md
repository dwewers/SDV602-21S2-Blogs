# SDV601 - Week 10 Blog

------

#### <u>Milestone Two Work</u>

------

This weeks focus was finalizing my work on milestone two of the assessment. I was getting close to finishing what was required of the assessment and was fixing up minor bugs, proof reading my code, commenting code, and changing variable and function names to follow the coding standards. There wasn't much in the way of learning this week as my focus was getting the aspects of my application finished.

I decided that I wanted to make a start on some features that would be present in the following milestone. These included such things as the upload and download features. Currently I am using MySQL, but may look into other methods of data storage such as MongoDB if I can't set up a remote SQL server.

**Below is my method for uploading data:**

This method defines two variables, data_dictionary and data_arr of which are referenced to variables in the global scope. I then call the `GetData()` method from the Data class and set the returned values to a local variable called "values." The GetData method returns two values of which we append the first value to data_arr and set data_dictionary to the second value. We then perform a for loop which generates the banners on the screen which will display the records to the user. These banners allow the user to click a button that opens a data view screen specific to that record in the table.

```python
class DataListScreen(Screen):    
    def upload_file(root, self):
        """[Data reader for uploading a csv file and generating the list of data calling the banner method]

        Args:
            root ([screen]): [the base screen of which the widgets are being added to]
        """
        global data_arr
        global data_dictionary
        
        values = Data.GetData(self, root, data_dictionary)
        if values == None:
            return
        else:
            data_arr.append(values[0])
            data_dictionary = values[1]
        for publicID, value  in data_dictionary.items():    
            if value[0] == "eventtype" or value[0] == "publicid":
                continue
            else:
                record = value
                magnitude = value[5]
                root.ids["grid_banner"].add_widget(Banner(title=publicID, operation=magnitude, root=root, record=record))
                pass
```



**Below is the GetData method:**

This uses the `askopenfilename()` method so that the user can select a CSV file from their local machine. If the user does not select a file, it will display an alert message saying "Please select a file." If a file is selected, we set a local variable called reader_ and set its value to the values read from the file using the `csv.reader()` method. A for loop then cycles through each row of the variable and updates the values in our data dictionary. We then create a data frame from the same CSV file for other uses. Both the data_arr and the data_dictionary variables are returned.

```python
def GetData(root, self, data_dictionary):
    """[The method for reading the data from the csv file]

    Args:
        root ([screen]): [the base screen of which the widgets are being added to]
        data_dictionary ([dictionary]): [the dictionary of data that we will add too when we retrieve data]

    Returns:
        [type]: [description]
    """        
    temp = Tk()
    temp.wm_state('iconic')
    
    filetypes = (
        ('CSV', '*.csv'),
        ('All files', '*.*')
    )

    filename = fd.askopenfilename(
        title='Open a file',
        initialdir='./geodata/',
        filetypes=filetypes)
    
    if filename is None:
        Alert(title='Error', text='Please select a file')
        temp.destroy()
        return
    
    if filename:
        with open(filename):
            reader_ = csv.reader(open(filename, 'r'), delimiter=',', quotechar='"')
            for row in reader_:
                data_dictionary.update({row[0]: [
                    row[1], row[2], row[3], row[4], row[5], row[6], row[7], row[8], row[9], row[10], row[11], row[12], row[13], row[14], row[15], row[16], row[17], row[18], row[19], row[20]
                ]})
                
            data_arr = pd.read_csv(filename)
            temp.destroy()
            return data_arr, data_dictionary
    else:
        Alert(title='Error', text='Please select a file')
        temp.destroy()
        return
```

**Downloading Data:**

The method for downloading the data wasn't as extensive as uploading it. All that was required was to use the `asksaveasfile()` method and use the file that is created to write too. We do this by using the pandas library to concatenate the data frames in the dataframe variable. This was done as when we upload the data, they are stored in an array as separate data frames (This will be changed though). We then convert the dataframe variable to a CSV file. 

```python
def download_file(root, self, data_arr):
    """[The method for merging and downloading the data to a csv file]

    Args:
        root ([screen]): [the base screen of which the widgets are being added to]
        data_arr ([array]): [the array in which the data is stored]
    """        
    temp = Tk()
    temp.wm_state('iconic')
    if (len(data_arr) <= 0):
        Alert(title='Error', text='No data to download')
    else:
        file = asksaveasfile(mode='w', defaultextension='.csv', filetypes=[("All Files","*.*"),("CSV Documents","*.csv")])
        if file is None:
                Alert(title='Error', text='Please screen a file')
                temp.destroy()
                return
        else:
            dataframe = pd.concat(data_arr)
            dataframe.to_csv(file, header=True, index = False, sep=',', encoding='utf-8', line_terminator='\n')
            temp.destroy()
```

Overall there wasn't really anything to learn here as it was just a process of getting the code finished. There will definitely be learning done in the future to improve this code and change the methods in which methods perform their tasks. There is definitely room for improvement and better ways of performing these tasks. I believe that this is a good learning experience as I am trying different ways of performing tasks, while still achieving the same end goal.
