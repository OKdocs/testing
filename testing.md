 #Testing

## The boxes

##### Static Analysis
Reviewing code line by line to find bugs. Pre-compiler makes also static analysis.

##### Dynamic testing
Runing program is tested with different testing methods.

### Black-Box testing (functional testing)

The source code is unknown to the tester while testing. Test cases are presented and compared with expected result. This is mainly testing the functionality of the program. This includes but is not limited to software verification answering the question: Are we building the right product?

#### User story
The user story is an informal, natural language desciption of one or more features of a software system. They can be written by possible end users or stakeholders. They facilliate sense making.

#### Use case
List of actions or event steps typically defining the interactions between a user and a program.

#### Decision table
A decision table shows all possible inputs (mainly if logical) and correct results. With non-boolean input and output only part of the decision table might be created.

#### Cause-effect graph
Directed graph that maps a set of causes to a set of effects. Causes can be inputs into program, the effects the returned response.

#### State transition table
Table that shows what state and what input will lead to which state and which output. States could be internal states a program is in.

#### Equivalence partitioning
Input data is devided into paritions of equivalent data from which test cases can be derived. Input from every parition is used, but not several inputs from the same partition. Example {1-100 = valid partition; 0-min = invalid parition; 101-max = invalid parition}

#### Boundary-value analysis
Input data is the edge cases at the edges of the equivalent partitions. In the example above this would be {0,1,100,101}.

#### Error guessing
Input data for test cases is established based on experience in prior testing or the software developers intuition.

### White-Box testing (structural testing)

The source code is known the the tester and can be analyzed. Inputs are chosen to exercise ideally all possible paths. Is usally implemented at the unit level, but can also be applied the integration and even systems level. 

#### Code coverage
Most or all of the code should be covered by the tests. Includes but not limited to
- function coverage
- statement coverage
- branch coverage
- condition coverage

#### Fault injection
Intentionally injection faults into the system to see how it fails and recovers. Included tests are 
- stress testing
- fuzz testing

## Testing Levels

### Unit testing
Tests run on function or single class/package level.

### Integration testing
Tests run on interfaces between components. Software components may be integrated in an iterative way or all together. 
Integration testing exposes defects in interaction between integrated components.

### System testing
Tests run on the whole system often involving several consecutive steps. In these tests the whole functionality of a finished system is tested.

### Operational acceptance testing 
Pre-release testing if the finished product meets the requirements and operates in different environments. Can also involve Beta-Testing.

## Testing types

## API testing
APIs get tested by providing input to API in a bread range including edge cases like unexpected or extreme inputs. Can even be performed on 3rd person APIs from dependencies. Best suited for test automatization.
- unit testing
- functional testing - multiple functions
- load testing - simulating large amout of users or big data processing
- runtime error detection - race conditions, exceptions, resource leaks
- web UI testing - browser, os compatability
- penetration testing - simulate attacker finding vulnerabilities
- fuzz testing - massive amounts of random data "worst case scenario"
 
## Continuous testing

Test are automated and performed after every change in the software. Important to speed up software development life cycle in Agile and DevOps.
This should be learned beIun.

- unit tests
- API testing
- integration testing
- system testing
- performance testing

Continuous testing should be designed to provide earliest possible detection of the risks that are most critical to the buissenes logic. Automated tests should focus on the API level, not the GUI level since they are easier to maintain. Tests should be executed at every update to version control.
When a problem is found, the tests should be adapted to test this more precise in the future.
