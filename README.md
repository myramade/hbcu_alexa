# Let's Build an Alexa Skill

You will be building the your skill front-end using the Alexa Developer Console and its backend using Lambda in the AWS Management Console. 

### Tools

For this activity, you will need:
1. your Amazon.com account login - the one you use to shop on Amazon.com
2. an AWS Educate account (if you are a student) or a personal aws.amazon.com account

## :vertical_traffic_light: Things Your Should Know :vertical_traffic_light:
Let's begin with an Alexa Skill theory crash course. Since we will get to building fairly quickly, there are a few things you should know:

- Basic Alexa Terminology
- Parts of an Alexa Skill
- Parts of a Voice Command
- Front-end - Interaction Model
- Backend - Hosted Service

### Terminology :rocket:
Let's start with some basic terms that you should understand. I've complied a list below (full glossary [here](https://developer.amazon.com/en-US/docs/alexa/ask-overviews/alexa-skills-kit-glossary.html)):

Terminology | Definition
------------|-------------
Amazon Resource Name (ARN) | Unique AWS resource identifier 
Automatic Speech Recognition (ASR) |	A technology that converts spoken words into text.
Intent	| An action that fulfills the users spoken request
Interaction Model |	The words user may say to make intents
Invocation |	The name of your Alexa skill
Lambda | a cloud service used to host and run code in response to a trigger without servers to manage
Natural Language Understanding (NLU) |	Technology used by computers to understand what a user’s words mean.
Slot |	An option argument in an intent.
Speech Synthesis Markup Language (SSML)	| A markup language to generate synthetic speech
Utterance	| The words a user says to Alexa to tell it what they want to respond to a question
Voice User Interface (VUI)	| A method for users to use voice to interact with and control an Alexa device


### Parts of an Alexa Skill

![Parts of an Alexa Skill](https://user-images.githubusercontent.com/28787937/72653217-bbd0cb80-393e-11ea-956b-3ce0d55b9061.png)

An Alexa skill has a frontend and a backend, just like a web application has a user-facing frontend and an operations backend.  In the case of an Alexa skill, since users interact with a Skill using their voice, the frontend is an Interaction Model called Voice User Interface. The backend for the skill we will build in this lab is a Lambda function, which is a serverless service that runs your code everytime it is triggered by an event. 

### Parts of a Voice Command
![Parts of a Voice Command]()



