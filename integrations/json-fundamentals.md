**JSON Overview: **When sending any type of API request, JSON is typically the delivery method of choice for most Alexa skills. 

JSON is a way to send information back and forth between two computers easily. While JSON might look intimidating at first glance, it's actually meant to be human readable first and foremost so with a little bit of practice, we should be able to work with it easily.

 **What is JSON?**

JavaScript Object Notation is a format that computers use to send information back and forth. For our purposes, we'll be using it to send information to our Alexa skills or to external codebases.

 ![img](https://downloads.intercomcdn.com/i/o/86306051/88f8e122c833648f698bd024/Screen+Shot+2018-11-18+at+8.39.30+PM.png)

In the above example JSON, we have some information about a super hero. This instance is focused on Superman. 

If we want to access any part of this JSON, we just need to use a command like the following



```
response.name
```

 If we were to store this in a variable in Voiceflow, the variable would hold the value "Superman".

We can use similar commands for any piece of data in a JSON



```
response.age
```

Will give us the value "32" when stored in a variable.

Where things might get a little bit tricky though is when we face an **Array** inside of a JSON. This is simply another way to group data together.

In the above example, "powers" is an array. In order to access the first power in this array, we would use the following command:



```
response.powers[0]
```

This would return the value "Flying" if we were to store it in a variable in Voiceflow.

Notice how the first item in the array corresponds to the number 0 and not the number 1. This is something that we need to keep in mind working with arrays. We always need to start counting from 0 and not from 1.

In the following example:



```
response.powers[2]
```

 This command would return the value "Laser Beam Eyes" from the array.

Here is a quick breakdown of how values in our array are counted:



```
0: Flying
1: Super Strength
2: Laser Beam Eyes
```

 **More Complex Examples:**

JSON is typically not as simple as the example posted above. We often find JSON objects nested inside other ones as shown below: ![img](https://downloads.intercomcdn.com/i/o/86309550/5a90affe847e1534ea09a3bd/Screen+Shot+2018-11-18+at+9.26.36+PM.png)

The enemies attribute adds a nested JSON object which contains an enemy called Lex Luthor.

If we want to access the data within this nested portion, we can use a command like the following:



```
response.enemies.LexLuthor.age
```

This would return us the value 33. As we in the above command, reaching into nested portions of our JSON is as simple as chaining the attribute we want to the end of our command.

In our final example, we'll access some data nested inside an array which is inside an object![img](https://downloads.intercomcdn.com/i/o/86310175/d85c885b760b20a267f419c9/Screen+Shot+2018-11-18+at+9.31.57+PM.png)

 If we want to access one of the powers of one of the enemies of Superman, we can use a command like the following:



```
response.enemies.LexLuthor.powers[0]
```

This command will return us the value "Mind Control".
