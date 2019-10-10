<p align="middle"><img height="160" src="https://api.featureninjas.com/assets/ti/83291560539879426.png"></p>

<p>
  <a href="https://trello.com/b/OhatDfJ3/fn-dev"><img src="https://img.shields.io/static/v1.svg?logo=github&label=GitHub%20Board&message=Open%20Backlog&color=007AC0&style=for-the-badge"></a>
  <a href="https://twitter.com/featureninjas"><img src="https://img.shields.io/static/v1.svg?logo=twitter&label=Twitter&message=Follow%20Us&color=08A0E9&style=for-the-badge"></a>
</p>

# Welcome Ninja!

This is the repository to track issues for FeatureNinjas SaaS. We have an agile and open mindset and therefore openly share our bugs and features that we work on with you.

You want to define what feature comes next? Head over to our GitHub project board at https://github.com/orgs/FeatureNinjas/projects/1 and give feedback in the issues there. 

To suggest new features or to report any bugs, create issues in this repository as you know from other GitHub projects.

# Get Started

1. Create a repository that will host your feature toggle configuration (if not done already). This can be public or private, be in a personal or organization account. (Note: You can use your projects source repository for the feature toggles as well, but we don't suggest to do so. Keep your configuration separate so that you can control who and when it is changed.)
2. In your feature toggle repository, create a `.featureninjas.yml` configuration file. It controls what the name of the file is that contains the feature toggles, and gives you the ability to specify an optional read token that can be used to additionally secure the API.

Sample:

```yaml
# Version information (is always 1.0)
version: 1.0

# (mandatory)
# Feature toggle file name
#   Contains the name of the file with the feature toggles.
file: fn-master.json

# (optional)
# Security Token
#   If this is set, then you have to provide this token via every request to
#   get your feature toggle configuration in the HTTPS header X-FeatureNinjas-Token
token: rtqoq85r1f6vejwuxtb1l
```

3. Push a feature toggle configuration to your feature toggle repository. The name of the file is specified in the configuration file (see previous step).

Sample:
```json
{
  "backupEnabled": true,
  "backupInterval": 10000,
  "backupFileFormats": "xlsx|psql|csv"
}
```

Have a look at the fn-sample-simple repository (https://github.com/FeatureNinjas/fn-sample-simple) for a very simple example of a feature toggle repository.

4. Use a simple HTTPS GET command to access your feature toggles from anywhere.

```bash
curl -X GET \
  https://api.featureninjas.com/t/<account-name>/<repo-name>/<branch_ref_name> \
  -H 'X-FeatureNinjas-Token: <token>'
```

This request always returns json in the body. The 'Accept' header is ignored.
