# Software development process
# Software Design
"Transforming a requirement specification into a detailed description of the software that is code ready."
- without techonology-specific, design without witch language they should use.
- might include pseudocod code, but not include implementation details
- decide classes methods data type to be used

## stage of design:
1. probelm understanding: most of this come from SRS document.
2. identify one or more solutions: TMTOWTDI, there's more than one way to do it.
3. describe solution abstractions
4. repeat process until "you can hand this design off to a development team that you don't know".


&nbsp;  

# Modularity:
Complex systems MUST be broken down into smaller parts.

## primary goals:
1. decomposability: broken down into smaller parts so it is easier to solve.
2. composability: reassembling most complex and difficult part.
3. ease of understanding: make communication easier.

## The four aspects of modularity:
1. Coupling: how well modules work together.
2. Cohesion: how well everything within a module fits together.
3. Information hiding: know what it dose not how (in most situations). Abstracting away implementation details make things simpler.
4. Data encapsulation: Containment of constructs and concepts within a module. For protecting the data and maintaining integrity. "If it get corrupted, it must been done by the module."

### Coupling:
We ensure that changes don't cross the boundaries between modules by loosing the coupling.
1. tight coupling:  
    1. content coupling: A relies directly on local data of B.
    2. common coupling: A and B both rely on global data.
    3. external coupling: modules rely on externally imposed format (or protocol or interface).
2. medium coupling:  
    1. control coupling: A controls the logical flow of B.
    2. data structure coupling: A and B both rely on the same composite data structure
3. loose coupling:  
    1. data coupling: modules only share parameters
    2. message coupling: modules only communicate through parameters or message passing.

### Cohesion:
Inheritance weakens cohesion, but it is usually a easy tradeoff.
1. weak cohesion:  
    1. coincidental cohesion: the code is in the same class or same file.
    2. temporal choesion: the code is activated at the same time.
    3. procedural choesion: the code is come after the other.
    4. logical accociation: the code is perform similar functions but separate.
2. medium cohesion:  
    1. communicational cohesion: operate on the same input or produce the same output.
    2. sequential cohesion: the code is the input of the other.
3. strong cohesion:  
    1. object cohesion: the code is for object attributes to be modified or inspected
    2. functional cohesion: the code is necessary for the function.


&nbsp;  

# Implementation
## coding tips!
1. program when you are alert (remember to take a break).
2. coding as self-documenting as possible ("comments describe the WHY and the code describe the HOW").
3. wirte comments, tests, and exception handling BEFORE writing functional code (test-driven development).
4. break long methods into manageable pieces (40 line is consider long).
5. "the class should be intuitive."
6. build methods preferably without side effects.
7. Don't repeat youself.
8. optimize only when necessary (and let the tools help).

## Deployment
planned steps, problem areas, and plans to recover.
### planning concerns
1. physical environment
2. hardware
3. documentation
4. training (deploy by trained developer)
5. database-related activities
6. third party sofware
7. software being deployed

## Rollback
keep production system alive when something went wrong.
"A matter of WHEN not IF".
prepare what the exact step and code you are going to do when rollback.
### point-of-no-return
At some point, rolling back will cost more than pushing through.
Know this point prior to deployment.
But still make sure you have the option to rollback.

## Coutover strategies
make sure your strategies is geolocation separately.
Test them to make sure it work when something really happen.
1. cold back-up (cold storage): have second machine, you need to deploy again. cheap but take more time.
2. warm standby: have second machine ready to go, one-click turn on (definition may be different). take less time.
3. hot failover: second system is on and ready, but not in production environment (different than load balancing). It is constantly being replicated (may have few minutes delay).

*******# Testing
"the process of finding errors".
start with small part of program that have completed (unit test).
test data (input)-> unit under test -> output -> oracle (check is it correct)

## definitions
- verification: confirm that the software performs and conforms to its specitcation. "Are we building the thing right?"
- validation: confirm that the software performs to the user's satisfaction. and assure that the software system meet the user's needs. "Are we building the right thing?"
- dynamic V & V: execute product and see what happend. that is Testing.
- static V & V: analyze the static system. like code review and pair programming.

## testing strategies
1. incremental testing (regression testing): test A and B, then test C with same test cases. You know what is change if errors occurred. If it works, then add more modules and test cases.
2. Top-down testing: you don't have level 2 module to take level 1 module's output as inpout. make a stub represent level 2 module. 
3. Bottom-up testing: similar to Top-down, but a stub is called a driver.
4. back to back testing: compare result of version 1 and version 2.
- additional resources  
faking, mocking, and stubbing  
https://stackoverflow.com/questions/346372/whats-the-difference-between-faking-mocking-and-stubbing

### axiomx of testing
- more bugs are detected , undetected bugs are probability also increase.
- you cannot test a program completely.
- you will run out of time before you run out of test cases.
- Testing will take more time then you want.

## test perspectives
1. white-box: you know what's inside. examines the internal design.
2. black-box: you don't know what's inside. based on requirements.
3. V & V Process: applied at each stage pf the process.

### stage of testing
1. unit teating: one class, for example.
2. module teating: set of units.
3. sub-system teating: collections of modules
4. system teating: full system.
5. acceptance teating: test by users. alpha or beta, for example.





