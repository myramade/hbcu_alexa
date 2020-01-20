> ![iconfinder_Oh_3713808](https://user-images.githubusercontent.com/28787937/72690305-ee5dfe00-3acf-11ea-8583-3e4fece3791c.png) *Hear Ye! Hear Ye! I've added all instructions for this lab on one page. Because, honestly, who wants to constantly click Next or Continue?*

# Let's Build Using the Alexa Developer Console
Now that you have the some basics down, let's start building. The first step is to access the Amazon Developer Console.  Don't confuse the Developer Console with the AWS Management Console; these are two separate platforms. The Developer console gives you access to resources you need to build an Alexa skill, an Andorid app/game, dash buttons, and more.   

## Logon to the Alexa Developer Console
To logon to the Alexa Developer Console, got to http://developer.amazon.com/

  * Enter the username and password you use to logon to the Amazon.com shopping website. If you don't have an Amazon.com account, you can quickly create one using your email address, no credit card needed. 

Once logged in, you'll see a few options on your screen, 
- Select **Alexa** under **Amazon Alexa**. 
- At the top of the Amazon Alexa screen click on **Skill Builders** and from the drop-down menu select **Developer Console**

## Create Your Skill

Now that you are logged on to the Alexa Developer console, let's create a new skill. 

- Click the **Create Skill** button. This will bring up the **Create a new skill** page. 

On the **Create a new skill** page, there's a few decisions points: 
* **Skill name** - this is the one to two-word name you're give your skill. It's the name users will see when you publish your skill. 
 * Type **Hello World**
* **Default Language** - you can decide which language you will use for your skill. I recommend English for now, you can add more langugages later. 
* **Choose a mdoel to add to your skill** - The peeps at AWS have created some pre-built model to simplify things; these are great for learning. For this lab, choose **Custom**.  A blue *SELECTED* banner will appear on the model you select. 
* **Choose a method to host your skill's backend resources** - on my intro page, I shared that your skill needs a backend.  The most common backend is a Lambda function. You are given a choice of three options, of which two are Alexa-Hosted. 
  * Select **Alexa-Hosted (Node.js)**
  
Once you make all your selections, click the **Create Skill** button at the top of the screen. 

This will take you the **Choose a template to add to your skill** page. Again, the AWS peeps has created some base templates you can use to create your skill, which is awesome. For this lab we are going to use the **Hello World skill**
 *  Select **Hello World Skill** template 
 *  Then click the **Choose** button at the top of the screen
 
>![iconfinder_Wait_132116](https://user-images.githubusercontent.com/28787937/72690247-4b0ce900-3acf-11ea-9c15-48692565d459.png) You'll see a modal pop-up on your screen as your skill builder is configured with your selections. Your Skill Builder screen will take a few minutes to load. This is a great time to take a few deep breaths!

# Skill Builder Page(s)

**Has your screen loaded?** 
It should look something like this (*I'm anti-screenshots when it comes to software because builds change constantly but felt you needed one here - be aware your screen may look a little or a lot different depending on when you are reading this*):
![alexa-developer](https://user-images.githubusercontent.com/28787937/72690352-80660680-3ad0-11ea-8214-8da381d36f6c.png)

**There is a lot of on this page, so take a minute to breath again - you got this**

This is the Skill Builder page. On the *left-side* of the screen, you'll see **Custom** and under:
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
* Under the *Skill builder checklist*, double click **Invocation Name** 
  * *Notice that **Invocation** on the left-side of the screen is now high-lighted.*
* On the **Invocation** page, the **Skill Invocation Name** is populated your skill name. 
* Change the skill invocation name -  Type **Yo World** in the box. 
  * *Anytime you make a change you will need to click **Save Model***
  
  
  



