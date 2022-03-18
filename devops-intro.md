# DevOps Into

## Refresh

Let's refresh our learnings from the previous session and run `npm run test`

I assume you can see now passing tests? Right?

So, this command which executes tests appears to be the beginning of the automation process.

We don't want to check out application manually every time, to answer the question: "Is it good enough to be published in production?"

## What is DevOps?

The word DevOps is a combination of the terms development and operations, meant to represent a collaborative or shared approach to the tasks performed by a company's application development and IT operations teams.

Ideally, DevOps means that an IT team writes software that perfectly meets user requirements, deploys without any wasted time and runs optimally on the first try. Organizations use a combination of culture and technology to pursue this goal.

To avoid wait times, IT teams use CI/CD pipelines and other automation to move code from one step of development and deployment to another. Teams review changes immediately and can enforce policies to ensure releases meet standards.

## Let's deliver the React app to Netlify

1. Almost every js-related project starts from `npm install` command, so, let's do it first to install our dependencies.
2. We can see `./build` folder appeared after command execution, and it contains our website's files.
3. Let's go to Netlify.com and register or login via github.com (it will ask to grant permissions).
4. I will use following [github action](https://github.com/marketplace/actions/netlify-actions) to make a deployment.
5. Let's have a look into [.github/workflows/deployment.yaml](.github/workflows/deployment.yaml) file.
6. There are few sections: dependencies, build, and deploy.
7. Let's discover Netlify logs and see the demo in here: https://andrewred.netlify.app/
8. Yay! 🎉 It works!

??? If enough time

6. Now it's time to create our access token, we need it to start making deployments from github. Visit page for doing this: https://app.netlify.com/user/applications (personal access token).
7. Let's speak about sensitive information, like tokens, passwords, etc. It's very important to keep it safe, so we're not going add it directly into our github workflow's code. Github provides a tool for it called [secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets), it keeps passwords encrypted and inject it into your workflow if needed.
8. Let's add token as a secret in github on the page `/settings/secrets/actions`

## Summary

DevOps is a set of tools and techniques which help automate daily developer's routines, prove the quality and sustainability of software, and deliver this software in an easy way to multiple environments.

Personally as a developer, when I get involved into DevOps I cannot stop myself in perfection of this topic. I started from simple workflow automation, pipelines building, CI/CD, and then creating infrastructure as a code in clouds.
I hope you will try this out and enjoy!
Thanks!
