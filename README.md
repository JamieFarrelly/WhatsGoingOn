# WhatsGoingOn

Inspired by [this script](https://gist.githubusercontent.com/LoranKloeze/e1cf5bb9f797b6128363d467d008ff0e/raw/e9ec7ab1546766a11fd9fbd889eefe5b30132012/whatsapp_phone_enumerator_floated_div.js)
which you can read more about in the blog post [Collecting huge amounts of data with WhatsApp](https://www.lorankloeze.nl/2017/05/07/collecting-huge-amounts-of-data-with-whatsapp/).

### WhatsGoingOn is a script to try to figure out whether 2 people have been chatting to each other on WhatsApp.

- Firstly it'll check if the first user is online every 10 seconds
- If they are online it'll then check to see if the second user has been online for the next 10 minutes (also checking every 10 seconds for the second user). 
- If the second user gets a hit too, a new row in the table will be outputted to the console which will tell you what time both users were online at.
- Repeat (after 10 minutes, to try avoid false positives)

To run:

- Log in to WhatsApp web as normal
- Open up the console in your browser
- Change the value of userA and userB to be a real mobile number (eg. 353851234567) in this script, make sure none have their status hidden (very few people do!)
- Copy and paste the file in to the console
- A message will appear along with a table which just has sample data for now
- If both users are online within the time periods set in this file (and mentioned above), a new row will be added to the table
- The rows include the time that userA was online along with the time that userB was online. Here's an example of what you could see in the console:
   ![example output](https://github.com/JamieFarrelly/WhatsGoingOn/blob/master/ExampleOutput.PNG)
- Leave running for whatever period of time you want

Notes:
The script could check online statues more often, but I've tried to keep the checks to a minimum while still making the script actually useful to some extent.
WhatsApp may throttle your calls to them or even ban your account, so don't use this with your main mobile number to be safe.
