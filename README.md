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

## :rocket: Terminology :rocket:
Let's start with some basic terms that you should understand. I've complied a list below (full glossary [here](https://developer.amazon.com/en-US/docs/alexa/ask-overviews/alexa-skills-kit-glossary.html)):

Terminology | Definition
------------|-------------
Amazon Resource Name (ARN) | Unique AWS resource identifier 
Automatic Speech Recognition (ASR) |	A technology that converts spoken words into text.
Backend | is the infrastucture that stores and arranges your data
Frontend | Presentation layer of an application. It's what your users interact with directly. 
Hosted Service | A service that is managed for you so you don't have to worry about updates, patches, scaling, etc
Intent	| An action that fulfills the users spoken request
Interaction Model |	The words user may say to make intents
Invocation |	The name of your Alexa skill
Lambda | a cloud service used to host and run code in response to a trigger without servers to manage
Natural Language Understanding (NLU) |	Technology used by computers to understand what a user’s words mean.
Slot |	An option argument in an intent.
Speech Synthesis Markup Language (SSML)	| A markup language to generate synthetic speech
Utterance	| The words a user says to Alexa to tell it what they want to respond to a question
Voice User Interface (VUI)	| A method for users to use voice to interact with and control an Alexa device


## Parts of an Alexa Skill

![Parts of an Alexa Skill](https://user-images.githubusercontent.com/28787937/72653217-bbd0cb80-393e-11ea-956b-3ce0d55b9061.png)

An Alexa skill has a frontend and a backend, just like a web application has a user-facing frontend and an operations backend.  In the case of an Alexa skill, since users interact with a Skill using their voice, the frontend is an Interaction Model called Voice User Interface. The backend for the skill we will build in this lab is a Lambda function, which is a serverless service that runs your code everytime it is triggered by an event. 

## Parts of a Voice Command
![Parts of a Voice Command](https://user-images.githubusercontent.com/28787937/72653601-8a58ff80-3940-11ea-835b-55dbd467711e.png)

Every Alexa skill has be be enabled and the user needs to interact with the skill using their voice. The graphic above breakdowns a voice command; this is the data that interaction model accepts to provide data back to the user. 

## Frontend - Interaction Model
![frontend](https://user-images.githubusercontent.com/28787937/72653624-a492dd80-3940-11ea-862f-c6ed02cac3cd.png)

Every application needs a frontend a way for your people to interact with your application. The Interaction Model defines the logic for the skill. The Voice User Interface (VUI) to map the user's _verbal input_ to the _intents_ your skill can handle. Utterances are the phrases a user may say – they help the skill connect the intents to words or phases spoken by the user. 

Let’s say you build a skill that does one thing, it responds only to the voice command in the image above. The skill will need an _intent_, we could name it _“DetergentIntent”_. The intent defines the behavior of a skill. The intent takes the user's _verbal command_ and triggers code in your backend. 

## Backend - Hosted Service

![backend](https://user-images.githubusercontent.com/28787937/72653645-baa09e00-3940-11ea-8e6d-8d10320c84a6.png)

Most applications today require some kind of backend that stores and arranges data. For skill you have to choose where your code will live, you have three options at this time: Provision Your Own (i.e. Lambda), Alexa-Hosted (Node.js), and Alexa-Hosted (Python). Think of the hosted service backend as your car engine, when you put the key in the ignition and turn your car on, your motor goes into action. When you stop the car and take the keys out of the ignition, your car is completely off - it doesn't idle.  

*IMPORTANT* 
_If you choose one of the two Alexa-Hosted options, be aware of the free-tier limitations.  If your skills goes viral, you'll want to consider moving it to your own Provisioned service like a Lambad function._








