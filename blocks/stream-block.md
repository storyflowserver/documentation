## **What you'll learn**

- What the stream block is and how it works
- How and when to use the Stream block

**Stream block overview** The stream block allows you to stream audio files longer than 90 seconds at a higher quality than the audio block. The stream block supports the following file types:

- MP3
- AAC/MP4
- HLS/M4U

You can learn more about the kinds of audio [files supported by Alexa skills here](https://learn.voiceflow.com/build-alexa-skills-without-coding/alexa-skill-audio-files).

**Stream block vs Audio block** The stream block works very differently than the [Audio block](https://learn.voiceflow.com/build-alexa-skills-without-coding/basic-blocks-tutorials/audio-blocks). Unlike the audio block, when a user hits your stream block - the user is **actually leaving your skill**. This functionality was built-in by Amazon. The user only returns to your skill if they say one of the Stream block's keyword functions. The accepted functions are below:

- Alexa, Pause
- Alexa, Next
- Alexa, Previous

Unless the user says one of these keywords while still streaming audio from the Stream block, your skill will be officially over. This is why it is suggested you use Audio blocks for almost all cases unless impossible. With Audio blocks, the user is still within your skill, and can access Command blocks and other in-skill features.

**Adding audio** To add audio files into the Stream block, you just need to drag and drop a supported audio file in of any length, or, you can tap & upload the file you want.

**Loop audio by default** When you enable 'Loop audio by default', you are looping the audio files within the Stream block until the user either stops the skill, or, if you have Audio player functions enabled, asks for an audio player function. This means that the audio will continue to loop until the skill is stopped, or the user asks 'Alexa, next/previous/stop/pause'. 

To enable loop audio, you can click the toggle button "**Loop Audio**" after clicking on the Stream button and opening the block settings:

![img](https://downloads.intercomcdn.com/i/o/110256032/27f7421b2bfb4e8a1870a480/image.png)

**Audio player functions** The stream blocks functions can be activated at any time when using the Stream block. For the user to activate a function, they must say the wake word followed by the function they desire (e.g 'Alexa, next').

With Voiceflow, you can determine what happens next when the user says one of the pre-defined Stream block functions by using the next and previous outputs of the block.

![img](https://downloads.intercomcdn.com/i/o/110256319/8c1fcde8c8498a5b4615f3a0/image.png)

When the user is in a Stream block and uses any of the pre-defined functions, they will be routed through the corresponding port. As an example, if the user says 'Alexa, next' while in your stream block - you can use a speak block and connect it to the next port, then have Alexa say the name of the next song before going into another stream block. That looks like this:

![img](https://downloads.intercomcdn.com/i/o/110256590/47a167eaf6eaadcc544fddd8/image.png)

You can also use the Custom pause option to add another output to the stream block so the user will be routed through the corresponding port if he says 'Alexa, pause'.

![img](https://downloads.intercomcdn.com/i/o/110256831/97973bdd68c3777738f728a3/image.png)

If the user says an Audio Player Command that does not have a connection, the skill will officially end. 

**Add M4U URL File** You can upload an audio file with the Add File button

![img](https://downloads.intercomcdn.com/i/o/110257554/9476c8852f495b1b24d181f3/image.png)

You can stream an M4U file by using the selecting the 'URL'. **You must use an https url because it is a requirement to pass the certification of your skill with Alexa.**

![img](https://downloads.intercomcdn.com/i/o/110257241/5797435774b942da3d0b312e/image.png)

You can also use a variable as an input for the URL

![img](https://downloads.intercomcdn.com/i/o/110257928/aa1b03ad2ca0c15f4b3cc248/image.png)
