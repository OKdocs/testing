 #Testing

## The boxes

### Static Analysis
Reviewing code line by line to find bugs. Pre-compiler makes also static analysis.

### Black-Box testing

The source code is unknown to the tester while testing. Test cases are presented and compared with expected result. Test functionality

### White-Box testing

The source code is known the the tester and can be analyzed. Inputs are chosen to exercise ideally all possible paths. Is usally implemented at the unit level, but can also be applied the integration and even systems level. 

#### API testing
APIs get tested by providing input to API in a bread range including edge cases like unexpected or extreme inputs. Can even be performed on 3rd person APIs from dependencies. Best suited for test automatization.
- [unit testing](#unit testing)
- functional testing - multiple functions
- load testing - simulating large amout of users or big data processing
- runtime error detection - race conditions, exceptions, resource leaks
- web UI testing - browser, os compatability
- penetration testing - simulate attacker finding vulnerabilities
- fuzz testing - massive amounts of random data "worst case scenario"

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

## Unit testing

Test cases are provided to function and result is checked against expectation. Should be build with while progamming, can even be written before each function is written.


## 



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
