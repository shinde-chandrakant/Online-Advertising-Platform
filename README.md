<p align="center">
  <a href="" rel="noopener">
   <img src="assets\img\giphy.webp" alt="Project logo"></a>
</p>
<h3 align="center">Online Advertising Platform  - (WIP) </h3>

<div align="center">


![ViewCount](https://views.whatilearened.today/views/github/shinde-chandrakant/Online-Advertising-Platform.svg?cache=remove)
![GitHub top language](https://img.shields.io/github/languages/top/shinde-chandrakant/Online-Advertising-Platform?style=flat)
![GitHub language count](https://img.shields.io/github/languages/count/shinde-chandrakant/Online-Advertising-Platform?style=flat)
![Stars Badge](https://img.shields.io/github/stars/shinde-chandrakant/Online-Advertising-Platform?style=flat)
![Forks Badge](https://img.shields.io/github/forks/shinde-chandrakant/Online-Advertising-Platform?style=flat)
![Pull Requests Badge](https://img.shields.io/github/issues-pr/shinde-chandrakant/Online-Advertising-Platform?style=flat)
[![Total Downloads](https://img.shields.io/github/downloads/shinde-chandrakant/Online-Advertising-Platform/total.svg)](https://github.com/shinde-chandrakant/Online-Advertising-Platform/releases/)
[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/shinde-chandrakant/Online-Advertising-Platform.svg)](https://github.com/shinde-chandrakant/Online-Advertising-Platform/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/shinde-chandrakant/Online-Advertising-Platform.svg)](https://github.com/shinde-chandrakant/Online-Advertising-Platform/pulls)

</div>

---

<p align="center"> This repository hosts a state-of-the-art Online Advertising Platform—a comprehensive big data project with components for efficient ad campaign management, seamless ad delivery, feedback collection, and detailed billing reports.
    <br> 
</p>

## 📝 Table of Contents

- [Problem Statement](#problem_statement)
- [Idea / Solution](#idea)
- [Dependencies / Limitations](#limitations)
- [Future Scope](#future_scope)
- [Setting up a local environment](#getting_started)
- [Usage](#usage)
- [Technology Stack](#tech_stack)
- [Contributing](../CONTRIBUTING.md)
- [Authors](#authors)
<!-- - [Acknowledgments](#acknowledgments) -->

## 🧐 Problem Statement <a name = "problem_statement"></a>

It is useful to design and follow a specific format when writing a problem statement. While there are several options
for doing this, the following is a simple and straightforward template often used in Business Analysis to maintain
focus on defining the problem.

- IDEAL: This section is used to describe the desired or “to be” state of the process or product. At large, this section
  should illustrate what the expected environment would look like once the solution is implemented.
- REALITY: This section is used to describe the current or “as is” state of the process or product.
- CONSEQUENCES: This section is used to describe the impacts on the business if the problem is not fixed or improved upon.
  This includes costs associated with loss of money, time, productivity, competitive advantage, and so forth.

Following this format will result in a workable document that can be used to understand the problem and elicit
requirements that will lead to a winning solution.

## 💡 Idea / Solution <a name = "idea"></a>

<p align="center">
<p>Make sure that we are configuring the EMR
    cluster properly.</p>

<p>We will need to make sure that we have <strong>Hadoop, Sqoop, Hive and
        Spark</strong> installed on wer cluster
    with <strong>Hue </strong>as an optional service. Also as an added step,
    make sure that in the <strong>Hardware
        configuration step</strong> for the EMR cluster
    generation,&nbsp;scroll down to the <strong>EBS Root Volume
        configuration</strong> and type the <strong>Root device EBS volume
        size</strong> as <strong>20
        GB.&nbsp;</strong></p>

<p>As part of the project, broadly we are required to perform the following
    tasks:</p>

<p><strong>Task 1:&nbsp;</strong>Setup MySQL Environment. we need to create
    "users", "ads" and "served_ads" table
    in MySQL using the given schema.</p>

<p><strong>Task 2:</strong>&nbsp;
    Writing Ad Manager using PyKafka. Here we need to read the data from
    Kafka then add the additional
    attributes followed by MySQL queries and finally printing the Campaign
    Id, Action &amp; Status on Console.</p>

<p><strong>Task 3:&nbsp;</strong>
    Writing Ad Slot Budget manager using MySQL Connector. Here we need to
    write a python script for slot
    budget calculation and updation. Here we also need to set up a proper
    cron job. In order to learn more about
    cron job, we can refer to the subsequent session of <strong>Additional
        Resources</strong>.&nbsp;
</p>

<p><strong>Task 4:&nbsp;</strong>
    Writing Ad Server using Flask &amp; MySQL Connector. Here we need to
    perform the following task:
</p>
<ol>
    <li>Write the API code using Flask.</li>
    <li>Performing the ad auction.</li>
</ol>

<p><strong>Task 5:&nbsp;</strong>
    Writing Feedback Handler using Flask &amp; MySQL Connector. Here we need
    to perform the following major
    tasks:
</p>
<ol>
    <li>Write the API code using Flask.</li>
    <li>Retrieve the entry from "served_ads" table.</li>
    <li>Add the additional attributes with the user feedback data.</li>
</ol>

<p><strong>Task 6:&nbsp;</strong>
    Writing User Feedback Writer using PySpark.
</p>

<p><strong>Task 7:&nbsp;</strong>
    Backing up Ad data from MySQL to Hive using Sqoop.
</p>

<p><strong>&nbsp;Task 8:&nbsp;</strong>
    Report Generator wherein we have to use Hive create table query for user
    feedback. Also, we need to
    generate reports based on the following parameters:
</p>
<ol>
    <li>
        Top 10 under-utilised Ad Campaign
    </li>
    <li>
        Top 10 spending Ad Campaign
    </li>
    <li>
        Total expenditure and CTR of the Ad Campaigns
    </li>
    <li>
        Top 5 Interactive(based on the CTR)
    </li>
    <li>
        Top 10 spending Ad Category
    </li>
    <li>
        Top Auction price differences.
    </li>
</ol>
</p>

## ⛓️ Dependencies / Limitations <a name = "limitations"></a>

- What are the dependencies of your project?
- Describe each limitation in detailed but concise terms
- Explain why each limitation exists
- Provide the reasons why each limitation could not be overcome using the method(s) chosen to acquire.
- Assess the impact of each limitation in relation to the overall findings and conclusions of your project, and if
  appropriate, describe how these limitations could point to the need for further research.

## 🚀 Future Scope <a name = "future_scope"></a>

Write about what you could not develop during the course of the Hackathon; and about what your project can achieve
in the future.

## 🏁 Getting Started <a name = "getting_started"></a>

These instructions will get you a copy of the project up and running on your local machine for development
and testing purposes. See [deployment](#deployment) for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them.

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running.

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

## 🎈 Usage <a name="usage"></a>

Add notes about how to use the system.

## ⛏️ Built With <a name = "tech_stack"></a>

- [MongoDB](https://www.mongodb.com/) - Database
- [Express](https://expressjs.com/) - Server Framework
- [VueJs](https://vuejs.org/) - Web Framework
- [NodeJs](https://nodejs.org/en/) - Server Environment

## ✍️ Authors <a name = "authors"></a>

- [@shinde-chandrakant](https://github.com/shinde-chandrakant) - Idea & Initial work

See also the list of [contributors](https://github.com/shinde-chandrakant/Online-Advertising-Platform/contributors)
who participated in this project.

<!-- ## 🎉 Acknowledgments <a name = "acknowledgments"></a>

- Hat tip to anyone whose code was used
- Inspiration
- References -->
