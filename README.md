# Let's Build an Alexa Skill

Have you ever wanted to build your own Alexa skill but need a starting point? I got you covered. In this lab you'll create your first Alexa skill in about 10 minutes. I reference Amazon AWS documentation and simplify some terms in order to help you wrap your brain around the basics. 

In this lab you are going to build an Alexa skill using different tools - from the the Alexa Developer Console, AWS Lambda, and Amazon Blueprints. 

### Tools

For this lab, you will need:
1. your Amazon.com account login - the one you use to shop on Amazon.com
2. an AWS Educate account (if you are a student) or a personal aws.amazon.com account

## Things Your Should Know 
Before you start building, let me give you an Alexa Skill theory crash course. Since we will get to building fairly quickly, there are a few things you should know:

- Basic Alexa Terminology
- Parts of an Alexa Skill
- Parts of a Voice Command
- Front-end - Interaction Model
- Backend - Hosted Service

## Terminology 
Let's start with some basic terms that you should understand. I've complied a list below (full glossary [here](https://developer.amazon.com/en-US/docs/alexa/ask-overviews/alexa-skills-kit-glossary.html)):

Terminology | Definition
------------|-------------
Amazon Resource Name (ARN) | unique AWS resource identifier 
Automatic Speech Recognition (ASR) |	a technology that converts spoken words into text.
Backend | is the infrastucture that stores and arranges your data
Frontend | the presentation layer of an application. It's what your users interact with directly. 
Hosted Service | a service that is managed for you so you don't have to worry about updates, patches, scaling, etc
Intent	| an action that fulfills the users spoken request
Interaction Model |	the words user may say to make intents
Invocation |	The name of your Alexa skill
Lambda | a cloud service used to host and run code in response to a trigger without servers to manage
Natural Language Understanding (NLU) |	technology used by computers to understand what a user’s words mean.
Slot |	an option argument in an intent.
Speech Synthesis Markup Language (SSML)	| a markup language to generate synthetic speech
Utterance	| the words a user says to Alexa to tell it what they want to respond to a question
Voice User Interface (VUI)	| a method for users to use voice to interact with and control an Alexa device


## Parts of an Alexa Skill 

![Parts of an Alexa Skill](https://user-images.githubusercontent.com/28787937/72653217-bbd0cb80-393e-11ea-956b-3ce0d55b9061.png)

An Alexa skill has a frontend and a backend, just like a web application has a user-facing frontend and an operations backend.  In the case of an Alexa skill, since users interact with a Skill using their voice, the frontend uses an Interaction Model called Voice User Interface (VUI). The backend for the skill you will build in this lab is a Lambda function, which is an AWS service that runs your code everytime it is triggered by an event. 


## Parts of a Voice Command 
![Parts of a Voice Command](https://user-images.githubusercontent.com/28787937/72653601-8a58ff80-3940-11ea-835b-55dbd467711e.png)

Every Alexa skill has be be enabled in order for users to interact with the skill using their voice. The graphic above breakdowns a voice command; this is the data that interaction model accepts to provide data back to the user. 


## Frontend - Interaction Model 
![intent](https://user-images.githubusercontent.com/28787937/72655149-ef642380-3947-11ea-8494-63a3de790a83.png)

Every application needs a frontend a way for your people to interact with your application. The Interaction Model, in this case the VUI defines the logic for the skill. The VUI maps the user's _verbal input_ to the _intents_ your skill can handle. Utterances are the phrases a user may say – they help the skill connect the intents to words or phases spoken by the user. 

For example, let’s say you build a skill that does one thing, it responds only to the voice command in the image above. The skill will need an _intent_, we could name it _“DetergentIntent”_. The intent defines the behavior of a skill. The intent takes the user's _verbal command_ and triggers code in your backend. 


## Backend - Hosted Service 
![backend](https://user-images.githubusercontent.com/28787937/72653645-baa09e00-3940-11ea-8e6d-8d10320c84a6.png)

Most applications today require some kind of backend that stores and arranges data. For skill you have to choose where your code will live, you have three options at this time: Provision Your Own (i.e. Lambda), Alexa-Hosted (Node.js), and Alexa-Hosted (Python). Think of the hosted service backend as your car engine, when you put the key in the ignition and turn your car on, your motor goes into action. When you stop the car and take the keys out of the ignition, your car is completely off - it doesn't idle.  

**IMPORTANT** 
_Alexa-Hosted options give you access to an AWS Lambda endpoint with data transfer lmintations. If your skills goes viral, you'll want to consider moving it to your own Provisioned service like a custom Lambda function._




[![button_get-started](https://user-images.githubusercontent.com/28787937/72658663-d324ae80-3968-11ea-8b1c-2d66a0f4f38b.png)](https://github.com/myramade/hbcu_alexa/blob/master/build.md)





