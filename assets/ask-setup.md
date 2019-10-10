# Alexa Skill Kit Setup and Workflow

Follow these steps to create an Alexa Skill with a team utilizing the ASK GUI, ASK CLI, and AWS. (This worked for our team, but does not create a "business" account on AWS).

**Once set up, do NOT use the Developer Console except for testing and distribution**

**We recommend setting up a secondary skill within the console to test any JSON object creation for Intents and their associated slots**

### GitHub Setup
* Create a GitHub organization
* Invite all members of your team to the organization
  * Adjust roles as necessary to ensure members can perform their correct actions
* Create an empty repo within the organization - do not initialize a `README.md`

### Amazon Service Setup
* Create an email account with GMAIL or email provider.
* Follow these next steps to create a Developer Account with Amazon and add your team to the account:
  * Create an account with `developer.amazon.com` using the team email account
  * Go to the [Alexa Developer Console](https://developer.amazon.com/alexa/console/ask), leave this window open to view the skill created after completing the ASK steps

* Follow these next steps to create an AWS Account with Amazon:
  * Create an account with `aws.amazon.com` using the team email account
  * Navigate to `IAM` to add the correction permissions to the account
  * Ensure there is a `User` for the Account and give it the following permissions:
    ```
    AWSLambdaFullAccess
    IAMFullAccess
    AmazonS3FullAccess
    CloudWatchFullAccess
    IAMUserChangePassword
    AWSLambdaExecute
    AWSLambdaBasicExecutionRole
    AmazonSNSFullAccess
    ```
  * Ensure these is a `Role` for the Lambda function and give it the following permissions:
    ```
    AmazonS3FullAccess
    AWSLambdaBasicExecution
    AmazonSNSFullAccess
    ```

* Follow these next steps to utilize the ASK CLI:
  * On a terminal run `npm install -g ask-cli`
  * Run `ask init` to set up a profile
    * Provide a name for the developer console profile (use the organization name)
    * Provide a name for the aws account profile (use the organization name)
      * Add the AWS access token
      * Add the AWS secret token
  * Run `ask new` to create a new Alexa Skill
    * Choose the correct runtime environment - either Python or Node.js
    * Choose the template you want to use
    * Give the skill a name
  * After initializing the code base, follow the GitHub instructions to add the repo as a remote push location for your code.
  * Run `ask deploy -p {PROFILE_NAME} --force` to deploy the skill to the developer console. (You can now return to the developer console to see your new skill)
    * **Whenever you run deploy it overwrites the data within the developer console**, this is where having a GitHub repo is important, it will allow you to manage branches between the various members of your team
  