## Access to other repositories fails during the build

Some builds require access to other private repositories for example to use as a dependency. Every project on the Codeship gets an SSH Key you can use to give us access to other private Github or Bitbucket repositories. You can find the SSH Key in your project configuration on the general page.

By default we only add the SSH key to the repository you've set up. If you need to give access to more repositories you can either add it to your own user account or create a machine user [as Github advises](https://help.github.com/articles/managing-deploy-keys).

An ssh key can only be added once to Github or Bitbucket, so make sure you remove it from the deployment keys of your GitHub repository first.

Typical error messages are

* remote: Repository not found
* fatal: Could not read from remote repository
* Permission denied (publickey).
