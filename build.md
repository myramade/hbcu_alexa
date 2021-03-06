> ![iconfinder_Oh_3713808](https://user-images.githubusercontent.com/28787937/72690305-ee5dfe00-3acf-11ea-8583-3e4fece3791c.png) *Sooo... I've added all instructions for this lab on one page. Because, honestly, who wants to constantly click Next or Continue?*

# Build Using the Alexa Developer Console
Now that you have the some basics down, let's start building. The first step is to access the **Alexa Developer Console**.  Don't confuse the Alexa Developer Console with the AWS Management Console; these are two separate platforms. The Alexa Developer console gives you access to resources you need to build an Alexa skill, an Andorid app/game, dash buttons, and more. The **AWS Management Console** gives you access to services that you can use to build a cloud architecture - that's a whole different topic.   

## Log-on to the Alexa Developer Console
To log-on to the Alexa Developer Console, go to http://developer.amazon.com/

  * Enter the username and password you use to log-on to the Amazon.com shopping website. If you don't have an Amazon.com account, you can quickly create one using your email address – no credit card needed. 

Once logged in, you'll see a few options on your screen:
- Select **Alexa** under **Amazon Alexa**. 
- At the top of the Amazon Alexa screen select **Skill Builders** and from the drop-down menu select **Developer Console**.

# Create Your Skill

Now that you are logged on to the Alexa Developer console, let's create a new Skill. 

- Click the **Create Skill** button. This will bring up the **Create a new Skill** page. 

On the **Create a new Skill** page, there are a few decisions points: 
* **Skill name** - This is the one or two word name that users will see when you publish your Skill. 
 * Type **Hello World**.
* **Default Language** - You can decide which language you will use for your skill. I recommend English for now, but you can add more languages later. 
* **Choose a model to add to your skill** - The peeps at AWS have created some pre-built models to simplify things; these are great for learning. For this lab, choose **Custom**.  A blue *SELECTED* banner will appear on the model you select. 
* **Choose a method to host your skill's backend resources** - On my intro page, I shared that your Skill needs a backend.  The most common backend is a Lambda function. You are given a choice of three options, two of which are Alexa-Hosted. 
  * Select **Alexa-Hosted (Node.js)**.
  
Once you make all your selections, click the **Create Skill** button at the top of the screen. 

This will take you to the **Choose a template to add to your Skill** page. Again, the AWS peeps have created some base templates you can use to create your Skill, which is awesome. For this lab, we are going to use the **Hello World Skill**.
 *  Select the **Hello World Skill** template. 
 *  Then click the **Choose** button at the top of the screen.
 
>![iconfinder_Wait_132116](https://user-images.githubusercontent.com/28787937/72690247-4b0ce900-3acf-11ea-9c15-48692565d459.png) You'll see a modal pop-up on your screen as your Skill builder is configured with your selections. Your Skill Builder screen will take a few minutes to load. This is a great time to take a few deep breaths!

# Skill Builder Page(s)

**Has your screen loaded?** 
It should look something like this (*I'm anti-screenshots when it comes to software because builds change constantly, but I felt we needed one here – be aware that your screen may look a little or a lot different depending on when you are reading this!*):
![alexa-developer](https://user-images.githubusercontent.com/28787937/72690352-80660680-3ad0-11ea-8214-8da381d36f6c.png)

**There is a lot of on this page, so take a minute to breathe again - you got this!**

This is the Skill Builder page. On the *left-side* of the screen, you'll see **Custom** and below that you'll see:
* Interaction Model
* Utterance Conflict
* Invocation
* Intents
* Slot Types
* JSON Editor
* and more...

The center of the screen, **How to get started** provides you with a bunch of great resources. I encourage you to check them out after you've completed this lab. 

On the *right-side of the screen, you'll see a **Skill builder checklist**.  Most of the items will have a green checkmark because we selected a pre-built template. *Yay us!*

Let's concentrate on working through the items in the checklist. 
## Invocation
The first item on the checklist is **Invocation Name**. This is where you set the word(s) a user will speak to launch your skill. 
* Under the *Skill builder checklist*, double click **Invocation Name**. 
  > *Notice that **Invocation** on the left-side of the screen is now highlighted.*
* On the **Invocation** page, the **Skill Invocation Name** is populated with your skill name. 
* Change the skill invocation name - (for example, you could use **yo world**). Keep in mind that this name cannot contain capital letters.
  > *Anytime you make a change you will need to click **Save Model***. 
  
## Intents
Let's move on to the **Intents**. This is how the VUI maps the user's verbal input to the intents your skill can handle.
* On the left-side bar you'll notice **Intents (#)**. Select the **HelloWorldIntent** under it. 
 > *The HelloWorldIntent was auto-created for you because you selected the Hello World template when you created the skill.  This Intent has some sample Utterances.*
* Add a few more Utterances - keep them short. Type additional Utterances in the text box and hit the **<Enter>** button on your keyboard to add the Utterance to the list of Sample. Need ideas? Try, Hello robot, What's up, How you doing...
* Once you've added the additional Utterances, click **Save Model*** and stay on this screen.
 > Make note of the sample Utterances – we'll use them in testing. 

## Build Model
Because you've made and saved changes to your Interaction Model, you will need to build your model in order for your changes to take effect. Just saving them is not sufficient. 
* Click **Build Model** at the top of the screen.

# Code
While your model is being built, let's edit some code. Click on the **Code** tab at the top of the screen. Let's take a few minutes to review the code in the index.js that is displayed on your screen. This code is written in JavaScript. 

Your code has two main functions: **_canHandle()_** and **_handle()_**. Here's what they do:
* The **canHandle()** function is where you defined which requests the handler responds to.
* The **handle()** function is where you define the response that is returned to the user. 

Can you read this code and predict what the Skill is going to do? 
 > Try to diagram the actions are happening in this code. 
 
Let's make some small edits to this code base:
* Change the first **handle()** _const SpeakOutput_.  Right now, the output when a user launches the Skill using the Invocation is: _'Welcome, you can say Hello or Help. Which would you like to try?'_. Type your own custom message here, be sure your text is in between the quotes (' ') and the line ends in a semicolon (;).

``` javascript 
handle(handlerInput) {
        const speakOutput = 'Welcome, you can say Hello or Help. Which would you like to try?';
```
        
 * After you edit the text, click the **Save** button and then the **Deploy** button at the top of the screen. 
  > *The **Deploy** button does not publish your skill. It's taking all of the lines of code in the codebase and copying it to an environment where it will be executed. 

# Test
We are ready to test your skill.  Click on the **Test** tab at the top of the screen. 
Notice **Test** is disabled by default and you have to enable it.  

* Select the dropdown menu next to **Skill testing is enabled in:** and change it from **Off** to **Development**.
> You'll now see the page is enabled.  On the left-side, you'll see **Alexa Simulator** is selected. Next to that, you'll see **Manual JSON** and **Voice & Tone**. 
* To test your skill, ensure **Alexa Simulator** is selected. 
* In the text box next to the selected language (_in this case English_), type **Open [Invocation Name]** and press _[Enter]_ on your keyboard.
 > Replace *Invocation Name* with the name you entered on the **Skill Builder** page. If you can't remember what you saved as your *Invocation Name*, you can click on the **Build** tab at the top of the page and then click on **Invocation** to copy your **Skill Inovcation Name**.
 
* Your skill will process the input you just provided and display the input/output (IO) processing on the right-side of your screen in JSON format. 

* Next, type one of the sample **Utterances** you configured in the **Build** page of the project and press _[Enter]_ on your keyboard.

![iconfinder_questionssvg_1579793](https://user-images.githubusercontent.com/28787937/72753439-c925ca00-3b79-11ea-9184-6cee9415ccbc.png)
**Did you get the expected response? If not, what went wrong?**


 <img width="571" alt="Screen Shot 2020-01-31 at 5 28 02 PM" src="https://user-images.githubusercontent.com/28787937/73578981-198d0980-444f-11ea-9f4e-522fde45b6bc.png">

# Was that too easy? I got you! Here's a challenge:

## _Can you make Alexa **whisper**?_

### Read the [documentation](https://developer.amazon.com/en-US/docs/alexa/custom-skills/speech-synthesis-markup-language-ssml-reference.html) and see if you can figure it out.  
  
  
  



