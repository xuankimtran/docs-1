# docs

Welcome to Katalon Docs! Here, you can find Katalon products documentation, manuals, guidelines, as well as tips and tricks to help you start a successful test automation journey.

To make the most out of Katalon Docs, we recommend you go over the documentation for each product to get an overview of the tools you will be working with.

## Products

As test automation becomes more crucial in today's technology landscape, it can be challenging to find an automation solution that is affordable, simple to set up, and comprehensive to meet a variety of automation needs.

To address these concerns, we initially created [Katalon TestOps](https://analytics.katalon.com/) and Katalon Studio as a set of innovative and cohesive Continuous Testing tools and services to help software development teams achieve Continous Delivery with confidence. Now, we have expanded our range to a variety of products to assist your automation testing needs. 

### Katalon Studio

Katalon Studio is a robust automation solution for Web, API, mobile, and desktop testing. It integrates all necessary components with built-in keywords and project templates into a complete automation framework. Katalon Studio is easy for beginners to use but offers advanced capabilities for expert users. This solution is trusted by an active community from 55K+ companies and 160+ countries around the world.

### Katalon TestOps

Katalon TestOps is a set of cloud-based services to help you streamline software quality by continuous test executions and intelligent analytics. As this moment, Katalon TestOps consists of the following services:
* Katalon TestOps Center: the test hub to gather and connect quality data from multiple sources, including Katalon Studio, JUnit, TestNG, and Jira.
* Katalon TestOps CI: the CI for managing test environments and scheduling remote executions on local machines, Kubernetes, and CircleCI. It is designed and built with ease of deployment and configuration in mind to let QAs focus on testing activities.
* Katalon TestOps Reports: provide dynamic perspectives and an insightful look at your automated testing activities.
* Katalon TestOps Vision: the visual-based testing service which is powered by AI to identify new defects on application GUIs quickly.

### Katalon Recorder

A Selenium IDE-compatible replacement on latest Chrome and Firefox versions. Katalon Recorder records, plays, debugs, manages automated tests, and exports to C#, Java, Ruby, Python, Groovy, or Robot Framework.

## Contribution Guidelines

We encourage you to help improve Katalon Docs by providing feedback, suggestions, or issues regarding our products. Below are several ways for you to contribute to Katalon documentation, including editing, requesting docs change, rating, or raising issues. Here are some suggestions:

-   Basic
    - Requests for docs change due to bugs, e.g. missed item, incorrect item, or confusing content
    - Typos or grammatical errors

-   Advanced
    - Reorganizing or rewriting docs content
    - New docs about Katalon Studio features

Please notice that although we very much appreciate all of your feedback, pull requests should be related to the documentation in this repository only.

## How to contribute

-   Katalon Knowledge Base is powered by [Github Pages](https://pages.github.com) and [Jekyll](https://jekyllrb.com/docs/) with source code hosted at https://github.com/katalon-studio/katalon-studio.github.io. You will need a [GitHub](https://github.com) account before making any contribution.
-   On the right menu, you can perform the following actions:

    - Edit this page will redirect you to the temporary repository of the related page. Fork this repository to make changes. Once finished, create a **Pull Request** to the master branch. Katalon team will complete a final review of the changes before publishing it to the community.
    - Request docs changes and raise docs issues can be filed at <https://github.com/katalon-studio/katalon-studio.github.io/issues>
    - Give feedback to the docs page by voting thumb up or thumb down.
    - Write new content for Katalon Knowledge Base. Simply fork the repository, make any modification, and send us a **Pull Request** for review.

## Development environment

### Linux

Install:

```
sudo apt update
sudo apt upgrade -y
sudo apt install -y build-essential ruby ruby-dev ruby-bundler
cd /mnt/d/docs
bundle install
```

Write:

```
cd /mnt/d/docs
bundle exec jekyll clean
bundle exec jekyll serve --watch --force_polling --incremental
```

View all files written by someone (on github):

```
git log --pretty="%H" --author="email" | while read commit_hash; do git show --oneline --name-only $commit_hash | tail -n+2; done | sort | uniq
```

## Katalon Community

For technical and product-specific questions, please post your questions to Katalon [forum](https://forum.katalon.com/discussions). We have a team of product specialists and community users to assist with your issues.

