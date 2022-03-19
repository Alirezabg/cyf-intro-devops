# DevOps Into

## Refresh

Let's refresh our learnings from the previous session and run `npm run test`

I assume you can see now passing tests? Right?

So, this command which executes tests appears to be the beginning of the automation process.

We don't want to check out application manually every time, to answer the question: "Is it good enough to be published in production?"

## What is DevOps?

DevOps (a portmanteau of “development” and “operations”) is the combination of practices and tools designed to increase an organization’s ability to deliver applications and services faster than traditional software development processes. This speed enables organizations to better serve their customers and compete more effectively in the market.

Ideally, DevOps means that an IT team writes software that perfectly meets user requirements, deploys without any wasted time and runs optimally on the first try.

To avoid wait times, IT teams use CI/CD pipelines and other automation to move code from one step of development and deployment to another.

DevOps engineer should focus on problem-solving and on their ability to increase efficiency, save time, and automate manual processes.

## Let's deliver the React app to Netlify

1. Almost every js-related project starts from `npm install` command, so, let's do it first to install our dependencies.
2. Now we need to build our project with command `npm run build`, so we receive the final version of the files ready to be delivered
3. We can see `./build` folder appeared after command execution, and it contains our website's files.
4. Now let's go to Netlify.com and register or login using our github.com (it will ask to grant permissions).
5. During your previous session you've done a github workflow for test execution and was amazing right?
6. So, today I want to do similar github workflow, but it will perform build and deploy of our application to Netlify.com.
7. Let's take a look into `.github/workflows/deployment.yaml`.
8. Let's discover Netlify logs and see the demo in here: https://andrewred.netlify.app/

??? If enough time

8. Now it's time to create our access token, we need it to start making deployments from github. Visit page for doing this: https://app.netlify.com/user/applications (personal access token).
9. Let's speak about sensitive information, like tokens, passwords, etc. It's very important to keep it safe, so we're not going add it directly into our github workflow's code. Github provides a tool for it called [secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets), it keeps passwords encrypted and inject it into your workflow if needed.
10. Let's add token as a secret in github on the page `/settings/secrets/actions`

11. Now let's try to create a pull request and see what happens.

12. Yay! 🎉 It works!

## Summary

DevOps is a set of tools and techniques which help automate daily developer's routines, prove the quality and sustainability of software, and deliver this software in an easy way to multiple environments.

Personally as a developer, when I get involved into DevOps I cannot stop myself in perfection of this topic. I started from simple workflow automation, pipelines building, CI/CD, and then finally creating infrastructure as a code in clouds.
I hope you will try to do DevOps too and enjoy it!
Thanks!
