Chatbot Cards
==============


==============
Text Card
==============

- Send Text Message to Subscriber.
- To add subscriber attribute, type { to display list of subscriber attribute, select an attribute from the list.
- To add system attribute, type [ to show list system attribute.



==============
Input Card
==============


- Create a question for subscriber and save the answer to an attribute.
- Type: validate the answer, default is Text
	- Email: require answer is an email.
	- Phone: requie answer is a phone number.
	- Number: answer must be a number.
	- URL: answer must be an URL( begin with http or https).
	- Date/Datetime: validate for Date/ Date with time value.
	- File/Image/Audio/Video: users must send a file through messenger.
	- Location: the answer must contain location value( long, lat).
- Save reponse to a Custom Field: select a custom attribute to send the answer to.
- Validate Message: message to user when their answers invalid.

==============
Email Card
==============
- Same as Input Card but it save the answer to System Email field of subscriber

==============
Phone Card
==============
- Same as Input Card but it save the answer to System Phone field of subscriber


==============
Livechat Card
==============

- This card pause Chatbot for a subscriber and send the conversation to an Admin.
- Start Message: Message send to user when the Chatbot paused and the livechat with human is started.
- Stop Message: Chatbot with this user is resume and notify user with this message.

- Timeout: the amount of time Livechat Human waiting for user reply. After this time with no response from user, Chatbot will resume and process the conversation with this user.

==============
Action Card
==============

- Define a list of actions:
 - Set/Remove User Attribute
 - Subscribe/Unsubscribe subscriber.

==============
Redirect Block Card
==============

- This card routes subscriber to a specific or random Block.
- User can filter the route base on user attribute.
 
==============
Subscribe Sequence/ Unsubscribe Sequence
==============

- Subscribe/ Unsubscribe a subscriber to a sequence.
- User can filter the route base on user attribute.

==============
Json Api
==============

- Send a HTTP GET or POST request to a specific URL.

==============
Google Sheet/ Mailchimp
==============

- Send Subscriber attribute to Google Sheet/ Mailchimp

==============
Send Email
==============

- Send an email to a specific email or user email if collected.
