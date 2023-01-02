# Google-Pensieve-a-Google-Data-Analysis
The average user stores huge amounts of data on Google and other cloud storage sites. Users are often not aware of the quantity of data that is stored over the years, and not careful about the type of information they store. An account breach could potentially lead to sensitive information to be leaked... which could be problematic.
Going through all of a user’s Google data online manually would be incredibly slow, and Google accounts offer many service, so there could be many years worth of data to sift through. How can all of this data be searched through efficiently? How can potentially sensitive data be flagged and shown to a user, so the user can be more aware of the data that they have, and should possibly be more careful with?

This project has two parts: an analyzer script and a visualization/GUI.

The analyzer program will look at all photos, emails, and text documents from Google Takeout (honestly, this will work for any mailbox/photos/documents - I guess they don't neccessarily have to be from Google, but that is the intended use case). An interesting expansion may be to add other social media data to the visualizations.

The photos will be analyzed using Google Vision and the new data will be appended to each photo's json metadata file.

The mailbox file for Gmail is analyzed; all emails are downloaded as text files and all attachments are downloaded and saved.
Metadata files for each type of data (photos from both Photos/Drive and emails, so far) will then be uploaded to Elasticsearch, along with the other text based documents.

After this, search will be available (powered by Elasticsearch) to search for anything in these newly updated json files.

All data that has a date will be saved in csv files with just a filename/minimal data

The visualization will show graphs of the data available from the analyzation.
