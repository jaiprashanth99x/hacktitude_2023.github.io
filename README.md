# Welcome to `Hacktitude.io`

>>DISCLAIMER: Please note that this project is created only for the purpose of Hacktitude.io and does NOT represent best practices of software development. The project contains purposefully placed errors, bad design practices, bad code quality and security malpractices.

1. [Setting up your environment](#setting-up-your-environment)
1. [Solving the challenges](#solving-the-challenges)
1. [Getting support](#getting-support)
1. [References](#references)

## Setting up your environment

This section helps you to understand the prerequisite required and how to work with the codebase. Please read through carefully and follow instructions to understand the codebase of this project.

### Prerequisites

Installations of latest stable versions of `Git`, `Node.js` and `npm` are required on your computer. You must also be proficient in working with the aforementioned technologies.

### Clone the project to your local computer

Git repository URL and credentials will be available at the start of the contest through a link. This link will be emailed to you.

Use Git to clone the project to the local development environment using your credentials. Please note that individual team members will have own git credentials, but the repository will be common for a team.

* git clone `<repository-url>`

### Installing dependencies

Once you clone the project from your team's Git repository, run the following command to install dependencies.

* `npm install`

### Validate if the environment is correctly setup

You can run the Sanity test file in the `tests` directory with the below command.

* `npm test -- _sanity`

If you have the environment correctly set up, all the tests should pass in the sanity test. If the sanity test fail, that is an indication of your environment setup issue, you must first attend to rectifying your development environment.

### Setting up the development database

Following commands will create a SQLite database called `main.sqlite` in your root folder for development purposes. The `migrate` command deletes the existing database and creates a new one with the DB schema, whereas `seed` command populates the DB with some initial data. These steps are required for running the application.

* to recreate the database
  * `npm run migrate`
* to populate initial data
  * `npm run seed`

>You may change `db/seed/**` files freely as you require. Once you change `seed` files run `npm run seed` to apply such to the database. Applied seed data will appear when you run the web application.

>However, tf you do data base schema changes with `migrations` ensure it doesn't break your test cases or the application.

### Building and running the application

To start the server (without nodemon) use the following command:

* `npm start`

Now the application should run at [http://localhost:3000](http://localhost:3000)

### How to navigate in the application

The system you are about to develop is an online, on-demand learning management system (similar to Coursera, Udemy, etc.). The functionality already available are straight forward to understand once you login to the system.

You can use the following credentials to login as an already existing user in seed data. Navigate the application using the main menu.

* Username: `abby@hacktitude.io` or `mary@hacktitude.io`
* Password: `test`

Alternatively you may create an user by yourself.

* Visit 'Sign Up' and Register a new user
* Login with the new credentials of the user you just created

### Executing the Tests

Use below commands to run the tests. When you FIRST run, all the tests except `_sanity.test` will fail. This is expected.

* To run all test:
  * `npm test`
* To run a single test file of a challenge: e.g.
  * `npm test challenge-0.test.js`
  * `npm test challenge-01`
  * `npm test challenge-02`

As you complete the challenges, respective tests will pass one by one. When you complete all the tasks of a challenge, all tests of the respective challenge should pass. Every Hacktitude challenge has a test case which you can run to validate successful completion of the challenge.

> NOTE: Tests are not using the main.sqlite database. Every test creates an an isolated in-memory database.

### Add .gitignore

You will note that the project code has no `.gitignore` file. Please add a `.gitignore` file with following content.

```
node_modules
main.sqlite
package-lock.json
```

>It is advised that one member of your team create the file, commit and push the .gitignore file to the remote repository with following commands.

* `git add .`
* `git commit -m "adding git ignore file`
* `git push`

Then other team members can pull the changes from the remote repository to receive the `.gitignore` file to their local machines.

* `git pull`

This is how you may use git to collaborate as a team in solving challenges.

### Legitimacy of your solution

Apart from the automated tests exposed to you, we will run additional tests on all awarding teams (the top 10) to verify that the team has not attempted to compromise the integrity of the tests. We will also conduct a manual developer review of the awarding teams' submissions.

Any attempt to compromise the integrity of the contest will `unconditionally disqualify` your team. Therefore please ensure you avoid attempting:

* Tampering files in the `test` folder or `config` folder
* Hard coding values or logic to pass the test without solving the challenge legitimately

### Improving your developer Experience (Optional)

This step is not mandatory to work on the Hacktitude challenges, but it may improve your development experience.  

* Install a plugin for SQLite on your IDE so that you are able to explore the SQLite database.
* Install a plugin for JEST testing on your IDE. This may allow you to run a test without depending on command line.
* Install any other plugin as necessary for you to improve your developer experience.

## Solving the challenges

If your sanity test pass and you are able to run the application, now you can proceed to the challenges. All the Hacktitude challenges are documented in an own file. Please visit the links below, read carefully and get started solving them.

Although the challenges are independent from one another, it will be easier for you to solve them somewhat sequentially to understand the challenges better.

Have fun!


## Getting support

There will be minimal to no support available on the context day. We are not in a position to clarify challenge descriptions on individual basis. However in case of a administrative need, you may contact the organizers via WhatsApp chat (No support for calls) to the phone number `0777046852`. If we answer a question, we may share your question (anonymously) and our answer, with all contestants via the common WhatsApp chat group you will be added to.

## References

* [Hacktitude official website](https://www.hacktitude.io){:target="_blank"}
* [Hacktitude FAQ](https://www.hacktitude.io/faq){:target="_blank"}
* [99x website](https://99x.io){:target="_blank"}
* [DevGrade website](https://devgrade.io/){:target="_blank"}

