
**Restful API testing using Tavern Framework**

Tavern-pytest API Automation and Integration automation test framework. Tavern is a pytest plugin, command-line tool and Python library for automated testing of RESTful APIs, with a simple, concise and flexible YAML-based syntax. It's very simple to get started, and highly customisable for complex tests.

The best way to use Tavern is with pytest. Tavern comes with a pytest plugin so that literally all you have to do is install pytest and Tavern, write your tests in .tavern.yaml files and run pytest. This means you get access to all of the pytest ecosystem and allows you to do all sorts of things like regularly run your tests against a test server and report failures or generate HTML reports.

You can also integrate Tavern into your own test framework or continuous integration setup using the Python library, or use the command line tool, tavern-ci with bash scripts and cron jobs.

https://tavern.readthedocs.io/en/latest/

**Quickstart**

Note that Tavern only supports Python 2.7 and up, and at the time of writing is only tested against Python 2.7/3.4-3.6.

$ pip install tavern


--test_WhatisISS.tavern.yaml

**Every test file has one or more tests...**
test_name: Get some fake data from the JSON placeholder API

**and each test has one or more stages (e.g. an HTTP request)**
stages:
   name: Make sure we have the right ID

  ** Define the request to be made...**
    request:
      url: https://api.wheretheiss.at/v1/satellites/25544/positions?timestamps=1436029892
      method: GET

   ** and the expected response code and body**
    response:
      status_code: 200
