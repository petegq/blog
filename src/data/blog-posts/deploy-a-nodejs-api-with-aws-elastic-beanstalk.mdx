---
title: Deploy a NodeJS API with AWS Elastic Beanstalk
publishDate: 13 May 2023
description: Deploy your Node.js API to Amazon Web Services (AWS) using the Elastic Beanstalk service.
---

Deploy your Node.js API to Amazon Web Services (AWS) using the Elastic Beanstalk service, which automatically handles the deployment, scaling, and maintenance of your application.

Here's a step-by-step guide to deploy your Node.js API to AWS Elastic Beanstalk:

1.  **Install the AWS CLI**: Install the [AWS Command Line Interface (CLI)](https://aws.amazon.com/cli/) on your local machine by following the instructions for your operating system.

2.  **Configure the AWS CLI**: Run `aws configure` in your terminal or command prompt and enter your AWS Access Key ID, Secret Access Key, default region name (e.g., `us-east-1`), and default output format (e.g., `json`).

3.  **Install the Elastic Beanstalk CLI**: Install the [Elastic Beanstalk Command Line Interface (EB CLI)](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html) on your local machine by following the instructions for your operating system.

4.  **Initialize the Elastic Beanstalk environment**: Navigate to your Node.js API project folder in your terminal or command prompt and run `eb init`. Follow the prompts to choose your region, create a new application or use an existing one, and configure your environment.

5.  **Create a `.ebextensions` folder**: In your project folder, create a new folder named `.ebextensions`. Inside this folder, create a file named `nodecommand.config` with the following content to tell Elastic Beanstalk to use the correct Node.js command for your app:

```yaml
option_settings:
	aws:elasticbeanstalk:container:nodejs:
		NodeCommand: "npm start"
```

This assumes you have a `start` script in your `package.json` file that runs your app, like this:

```json
"scripts": {
	"start": "node app.js"
}
```

1.  **Deploy your app**: Run `eb create` in your terminal or command prompt to create a new environment and deploy your Node.js API. The command will prompt you for an environment name and a DNS CNAME prefix (choose a unique name). It will then package your app, create an environment, and deploy your app to AWS Elastic Beanstalk.
2.  **Monitor your app**: Run `eb open` to open your deployed app in the browser. You can also run `eb status` to check the status of your environment, and `eb logs` to view logs.
3.  **Update your app**: To deploy an updated version of your app, run `eb deploy`.

Remember to update your API's base URL to point to the Elastic Beanstalk environment URL in your client applications.

For more information, refer to the [official AWS Elastic Beanstalk documentation for Node.js](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_nodejs.html).
