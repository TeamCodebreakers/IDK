# Team Code Breakers: General Project Description

### Members
* Melfi Perez
* Nick Paro
* Jack Kinne
* Matt Stuhring

### Summary of idea
* We want an Alexa Skill that suggests places to eat by making a call to the Yelp Api and returning restaurant recommendations, by saying "Alexa, open FeedMeNow".  
* This connects to S3 bucket with lambdas to allow persistence throughout the skill session & to allow the user to add multiple members to a group.  

### What problem or pain point does it solve? 
* This eliminates the headache of trying to choose a restaurant when you don't know what you want to eat.  
* The intention is to reduce "hanger" and indecision about food choices, especially in group conversations.  

### Minimum MVP definition.What is the minimum required for you to present on your demo day?
* Alexa skill.
* Engaged invocation phrases.  
* With utterances which we capture and manipulate.  
* Yelp API to gather local restaurants.
* Uses the following AWS services:  
* Lambda.
* IAM.
* SNS.
* CloudWatch.
* S3.
