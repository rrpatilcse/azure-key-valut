# add-azure-secrets

This adds secrets to the azure key vault. Usually you manually add secrets to key vault, which is long and tedious process, & currently available libraries require lots of processing to authenticate & add secrets. The "add-azure-secrets" will simplify all the process and help you to automate adding secrets to the azure key vault.

Authenticate application by client ID and client secret & use your key vault URI to add secrets.


## Installing

```
npm i add-azure-secrets
```

## Versioning

We use [SemVer](http://semver.org/) for versioning.

## Example

```
let secretClient = require('add-azure-secrets');

async function configureKeyVaultValues() {
    let secrets = [
        {
            Name: 'database',
            Value: 'db-name'
        },
        {
            Name: 'database-password',
            Value: 'db-password'
        }
    ]
    let applicationID = '';
    let applicationSecret = '';
    let vaultURL = '';
    await secretClient.addSecrets(applicationID, applicationSecret, vaultURL, secrets);
}
```

## Authors

* **Rahul Patil**

See also the list of [contributors](https://github.com/rrpatilcse/azure-key-valut/graphs/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
