A `webhook` is something that will call your application when something on GitHub happens.

![Image of GitHub Webook](https://github.com/arjungoel/GitHub_Actions/blob/feature/images/github_webhook.PNG)



**GitHub Apps**:

- You can integrate your custom applications with GitHub by listening to `webhooks` on events.
- You can integrate your custom functionality, and you can build and test with CI/CD workflows across Linux, Windows and macOS. 

In short GitHub Actions are:

- Repository automation to respond to GitHub events.
- CI/CD build and test functionality.
- Linux, Windows and macOS runners in the cloud.

When you click `Actions` option of a GitHub Repo:

1. The first thing GitHub does is it scans your repository using a tool called `linguist` to look at what is in your repository.

> NOTE: `GitHub Actions` is all defined by YAML Language.


**Unpacking/Demistifying the YAML File**:

1. Every workflow has a name. 
2. Then we have `[on]` clause which means how you trigger things.
3. Then it define `jobs`. Jobs will run in parallel on different machines.
4. Then there is a `matrix` support. A matrix lets you easily define a piece of workflow and then repeat it.	


`gollum` is the internalish name for the `Wiki` used by GitHub. So all of its webhooks are still called gollum for the wiki.



**GitHub Actions NDC**:

DevOps is the union of people, process and products to enable continuous delivery of value to your end users.

GitHub Action is a workflow system. It can trigger any workflow or any event inside of github.

GitHub Actions is the product name and you build workflows using that.

- `Workflows` allows you to do is specify the process that you want to happen.
- They belong in YAML files (whitespace sensitive) in a special directory in your repository, `.github/workflows`.
- Workflows are triggered on events. e.g. push, `pull_request`, public, schedule, `workflow_dispatch` (manual trigger).

In addition to being called `GitHub Actions as a product`, there are also things to add to your workflows which are called `Actions`.

- Actions are tasks are reusable units of code that could be used by your different workflow files. You can build your own actions or can go to marketplace and create actions using NodeJS or containers using any language.
- They are referenced from workflows as `uses:owner/repo@ref`.

Examples:

* Stale Actions: You can scan your repo for issues and pull requests that haven't been touched in a while.
* Azure WebApp Action


`Secrets` are encrypted variables you can create in an organization, repository, or repository environment.

Environments are currently in beta phase. You can take the jobs in your workflow and target those environments and when you target a job at an environment you can define rules such as `required reviewers`, `wait timers` and `environment level secrets`.

Each job defined in your workflow runs on it's own runner.
- A job is made up of series of steps and these steps are the actions the tasks that you want to take in the job.
- A job can have one step or multiple steps.
