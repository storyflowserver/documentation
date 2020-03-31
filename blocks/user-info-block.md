## What you'll learn 

- How to pull emails, phone numbers, and names from users
- Use the Customer Profile API (Alexa)
- Access user Amazon profile information

**Video tutorial**

**User Info and Permissions block overview** The User Info and Permissions blocks allows you to ask users for information from their Amazon account - such as their email, name, and phone number. For more technical users, this uses the Alexa Customer Profiles API. 

Users will be given a permissions card when downloading your skill asking for their info. Users can accept, or decline to give you their permissions - and which ones they do give. 

![img](https://downloads.intercomcdn.com/i/o/110272712/97eaf2308c1907b12003f49c/image.png)

Permitted user emails, phone numbers, and names are stored in variables set by the creator.

![img](https://downloads.intercomcdn.com/i/o/110272810/72bbbc5b464282b4887273bf/image.png)

**User Info Success block port** The success block port is not labeled. When permissions are granted, and transferred to your selected variables, the skill will follow the success path.

**User Info Fail block port** The failed block port will activate when the users decline to give your skill the requested permissions or permissions request fails.

The use is therefore as follows: Within the user info block you select the information you want to obtain, if the user has not yet authorized your skill the path will follow the fail port. On this port you connect the Permission block that will generate the card in the Alexa application and on [alexa.amazon.com](http://alexa.amazon.com/) The user will have to accept this request for you to get this information. A good practice is to use a speak block on the output port of the Permission block with a message of the type: 'Our skill requires access to your email, please authorize our skill in your Alexa application or from [alexa.amazon.com](http://alexa.amazon.com/) and restart the skill again.'
