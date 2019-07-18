<p align="middle"><img height="160" src="https://api.featureninjas.com/assets/ti/83291560539879426.png"></p>

<p>
  <a href="https://trello.com/b/OhatDfJ3/fn-dev"><img src="https://img.shields.io/static/v1.svg?logo=trello&label=Trello&message=Open%20Backlog&color=007AC0&style=for-the-badge"></a>
  <a href=""><img src="https://img.shields.io/static/v1.svg?logo=twitter&label=Twitter&message=Follow%20Us&color=08A0E9&style=for-the-badge"></a>
</p>

# Welcome Ninja!

This is the repository to track issues for FeatureNinjas SaaS. We have an agile and open mindset and therefore openly share our bugs and features that we work on with you.

You want to define what feature comes next? Head over to our Trello board at https://trello.com/b/OhatDfJ3/fn-dev and vote for the features that are important to you. You can even add comments if you feel that something is missing.

If you want to suggest new features, add an issue here in the repository with the label "enhancement". We will then move it to Trello. Moved suggestions will be closed and furthermore tracked in the Trello Board.

**Why are we using Trello instead of GitHub Projects?** Because Trello allows you to vote on cards. This helps us to prioritze directly based on your feedback.

For bug reports, create issues in this repository as you know from other GitHub projects.

# Get Started

1. Create a repository that will host your feature toggle configuration. This can be public or private, be in a personal or organization account. (Note: You can use your projects source directory for the feature toggle configuration, but we don't suggest to do so. Keep your configuration separate so that you can control who and when it is changed.)
2. FeatureNinjas is currently in Beta. To get started, send an eMail to stephan@featureninjas.com and request access. After you are given access, you will receive an eMail with a link to connect FeatureNinjas to your GitHub account. 
3. Push a feature toggle configuration to your repository, created in step 1 and that you connected FeatureNinjas to in step 2. The name of the configuration file is currently limited to `fn-master.json`.

Sample:
```json
{
  "backupEnabled": true,
  "backupInterval": 10000,
  "backupFileFormats": "xlsx|psql|csv"
}
```    
4. Use a simple HTTPS GET command to access your feature toggles from anywhere.

```
curl ...
```
