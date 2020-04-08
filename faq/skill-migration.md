# Migrating a Live Skill

How to manually update your Amazon Skill ID



If you need to make edits to a live Alexa Skill, but that skill is not linked to a current Voiceflow project, you can re-build the skill in Voiceflow and manually update the Amazon Skill ID associated to it. 

To start, open your project in Voiceflow. 

![img](https://downloads.intercomcdn.com/i/o/118055117/ab234ec7462890f3ef55eff5/migrate.png)

The next step is to copy your skill's URL and change the word "canvas" to "migrate" 

before: https://creator.voiceflow.com/**canvas**/nkdwQA7mKr/f8554e39cf90bf5b8474aca99bdf683b
after:
https://creator.voiceflow.com/**migrate**/nkdwQA7mKr/f8554e39cf90bf5b8474aca99bdf683b

You'll then see this page: 

![img](https://downloads.intercomcdn.com/i/o/118056469/c5e55d8711612ddc8b2cbac2/SMT.png)

Now, you can enter your Amazon Skill ID, and voila! Your existing Voiceflow project is now linked to your live Amazon Skill. 

#### Need help finding your Skill ID? 

After uploading your project to the [Alexa Developer Console](https://developer.amazon.com/alexa/console/ask) (ADC), under the name of your skill, there's a button that says View Skill ID. 

![img](https://downloads.intercomcdn.com/i/o/118070475/878b197991024bee6cb247d1/adc.png)

![img](https://downloads.intercomcdn.com/i/o/118070540/cd1aa62eee47cfec26acb2a5/skill+ID.png)


The skill ID is quite long and looks like this:

**amzn1.ask.skill.e7ad7de6-51f6-4acc-8b48-a74eb56385c4**
