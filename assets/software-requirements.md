## Vision
- The vision of this product is to make an easy, voice interface for suggesting food choices.  
- We want to save options, limit by distance, and eventually use this for groups and send texts with addresses.  

## What pain point does this project solve?
- This eliminates the headache of trying to choose a restaurant when you don't know what you want to eat. 
- The intention is to reduce "hanger" and indecision about food choices, especially in group conversations.  


## Why should we care about your product?
- Its easy, it's helpful, it reduces stress especially for couples and groups.
- It's hard to make choices when you're hungry.  So don't. 


## Scope (In/Out)
### IN - What will your product do
- allow voice to alexa.
- allow option settings.
- limit recommendations by area.
- get data from yelp API
- save and persist data


### OUT - What will your product not do.
- Will not reserve a table at a location.
- Will not have a GUI interface


## MVP
What will your MVP be. What is your expected minimum end product?
- Alexa skill.
- Engaged invocation phrases. 
- With utterances which we capture and manipulate.  
- Yelp API to gather local restaurants.
- Uses the following AWS services:  
- Codestar. 
- DynamoDB.
- Lambda.
- IAM.
- S3.

## Stretch
- groups
- texts
- books
- other cateogory searches

## Functional Requirements
- A user can ask for a restaurant
- a user can set location distance
- a user can set a type of food they hate
- a user can persist preferences
- A user can update preferences

## Non-Functional Requirements (301 & 401 only)
- Usability Testing
We will be focusing on usability and integration testing for voice activation of utterances, to ensure a good product and
responsive architecture.
- Ease of Access
This product must be easy for users to engage with, with references our previous point.  Saving options must be quick, so we
will include a default or custom option to start, in case a user needs a recommendation immediately.  Being quick is critical, 
as we want to be a source of relief and not stress for the userbase. 

## Data Flow
![data_flow]()
