# Testing 101

## Approaches to delivering a product

### Waterfall 

Requirements -> development -> test -> operator/deployment

Could static test on requirements: why do we want these requirements?
Time period from requirements to test can last as long as 2 years or more.

Unit testing on development stage.

Functional
Integration testing in testing stage: API, DB.
Test scenarios - > test steps (do this, do that)

Non-functional
Performance: traffic through websites. 


Standards: ISTQB IEEE829

Unit testing coverage: Prioritise high risk areas, usually around 70-80%.

### Agile

4 agile principles.

1. Individuals and Interactions Over Processes and Tools
2. Working Software Over Comprehensive Documentation
3. Customer Collaboration Over Contract Negotiation
4. Responding to Change Over Following a Plan

SCRUM is an agile delivery methodology.

### Continuous Integration

Branching off from github and multiple people working on their branch.  They may be working on a specific class and if another contributor is working on the same thing they need to communicate to one another.

If branching then to make sure to frequently pull and push your work so people can get the updated version.

Use this method to create updates too.

## RSPEC

Ruby framework for ruby testing.

### TDD

Test driven development
Fail -> Pass -> Refactor(make the pass neat).

Relishapp.com for documentation on

## V model and software delivery lifecycle

__Unit test__

* Functional: making sure buttons works etc
* Integration: making sure two elements that communicate with one another work.
* Deployment
* Non-functional: traffic
* BAU + DR: disaster recovery (making up for lost profits)
* Monitoring: checking when the app fails/slows down.

## White box testing
You know how it works: you can see the code, database and data sources.


## Black box testing
You don't know how it works: you can't see the code, database and data sources.






