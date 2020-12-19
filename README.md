# Web Scraping Site Data into Excel

I received a query from a friend the other day: how would you take numerical data from a webpage and pull it into an Excel worksheet? This friend works in an office that does not normally deal with Python or other languages designed for controlling data. It had to be done with Excel for ease of use. My experience in web scraping is almost entirely in Python, so this query presented a new challenge for me. After dabbling with this process and finding some success, here are the steps I took:

## 1. Open the Inspector

Once your desired webpage is open(shown below), right-click in some blank space. The drop-down menu will include a command called “Inspect”. Click this command, and a window will open showing the code behind the webpage.

## 2. Use the Network Tab

Once the inspector is open, click the Network tab. If this tab appears empty, refresh the webpage. This will show you every file on the page as the browser loads it. Once everything has loaded, the column “Type” will tell you the type of each file. We are looking for daily weather data in this case, which will likely be in XHR files. XHR stands for XML HTTP Request. You may have to search through the different files to find the ones that are most useful to you. This is sometimes obvious: files that contain data will be more useful than “Media” or “Img” types. This will be covered further in the following steps.

## 3. Open a JSON Tab

Once you find the file containing the data you want, right-click its name and select “Open in new tab”. A tab will open, containing the data in JSON format. To help with clarity, I recommend using a browser extension that makes JSON easier to read. I use JSONView for Google Chrome, which is available for free in the Chrome Web Store. If you use a different browser, search “json view extension” for more options. Read through this tab and see if it contains the data you need. In this case, this would be the first file listed in the Network tab. Reading the code, we can see detailed weather information given for specific periods of time. This was relevant to the initial query I received. As such, I’ll move forward with this data for now.

## 4. Convert JSON to CSV

There are several ways to convert JSON into a CSV file. When possible, I prefer simple methods. I use an in-browser converter found at this address: https://konklone.io/json/. You’ll see that it turns the JSON file into a table of data. This website also contains a link to download the resulting CSV file. As is says, this converter may struggle with extremely large files. As I learn more about this process, I stay on the lookout for to convert JSON files containing heavy amounts of data.

## 5. Download the File

After clicking the link to download, we can now see our CSV file containing the data from the webpage. It can now be opened in Excel and saved as a .xlsx file, or in another format.

---

I hope that this tutorial has been informative and clear. These are the preliminary steps to this process, but it is naturally possible to go into much more detail and precision. I was able to answer my friend’s original questions, but I am still on a journey of learning and honing these skills.