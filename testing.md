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

### Installation testing
Tests whether the software can be installed, uninstalled or updated using various options. The process can also be ended or made fail to test how the software is behaving in case of unexpected abort. Is part of Operational acceptance testing

### Compatibility testing
Tests how the software runs on different target environments, like os or browser in case of a web service. Sometimes such issues can be fixed by abstracting os functionality into a separate module. Docker should also avoid this problem at large.

### Smoke and sanity testing
Also called build verification test (BVT). Very quick test to see if the result of a function is completely wrong or not. Is used as first test, to evaluate if further testing is worth the effort. Can be used as first unit test and as first test for the whole system. Daily smoke tests are industry best practice.

### Regression testing
Tests that were previously run to expose bugs are run again after updates or other bugfixes. It is considered good coding practice to record a test that exposed a bug and rerun it after subsequent changes to the program. 

### API testing
APIs get tested by providing input to API in a bread range including edge cases like unexpected or extreme inputs. Can even be performed on 3rd person APIs from dependencies. Best suited for test automatization.
- unit testing
- functional testing 
- load testing
- runtime error detection - race conditions, exceptions, resource leaks
- web UI testing - browser, os compatability
- penetration testing 
- fuzz testing 
 
### Continuous testing

Test are automated and performed after every change in the software. Important to speed up software development life cycle in Agile and DevOps.
This should be learned beIun.

- unit tests
- API testing
- integration testing
- system testing
- performance testing

Continuous testing should be designed to provide earliest possible detection of the risks that are most critical to the buissenes logic. Automated tests should focus on the API level, not the GUI level since they are easier to maintain. Tests should be executed at every update to version control.
When a problem is found, the tests should be adapted to test this more precise in the future.

### Destructive testing
Tries to cause the software or subsystem to fail. 
#### Stess testing 
Tries to overload parts of the system to make the component fail and therefore the system crashes.

#### Load testing 
Simulating large amout of users or big data processing on the system as a whole to examine how it behaves at or above maximum capacity.

#### Volume testing
Test performance when a certain components like a file or a database increases enormously in size.

#### Fuzz testing
Massive amount of random data flood the input. Should be a "worst case scenario".

### Software performance testing
Verifies or qualifies attributes of the software like scalability (e.g. load testing), reliability (e.g. stress testing) or resource usage (e.g. benchmark testing)

### Security and penetration testing
Simulate attacker finding vulnerabilities, or be the hacker or hire white-hat hackers.

### Development testing
Broad spectrum of defect prevention in order to reduce software development risks, time and costs. It performed by the developer during construction phase. Can include but not limited to: static code analysis, data flow analysis, metrics analysis, peer code reviews, unit testing, code coverage analysis, taceability, and other software testing practices.

### A/B testing
Two versions of software are compared. Custumers are either routed to one or the other. Data is collected to deternime which version is better.

### Concurrent testing
Test whether program runs correctly when running concurrent.

### Acceptance testing
Customer runs the software in his environment on his hardware.

#### Alpha testing
Users, customers or and independet test team tests the software at the develper's site.

#### Beta testing
Beta versions of the software are released to a limited audience outside of the programming team.

#### Usability testing
Checks whether the interface is easy to use and understand.

#### Accessibility testing
Checks whether software is accessible for someone not using on one sense or extremity. For example: can you use voice control instead of touch, can you get auditory feedback instead of visual feedback, are subtitles available.
