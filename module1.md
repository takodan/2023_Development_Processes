# Software development process
# what sofware development looks like
like building a house
### waterfall method phases:
1. requirements: what exactly you need to build.
2. architecture: design the system.
3. implementation: start coding, unit testing
4. verification: integration testing, user acceptance testing
5. Operations and maintenance  
- this method has some problem like misinterpretations, intergration issues, etc.  

### Agile
It's not a model. It's a mindset (manifesto and principles).
Change is norm, build sofware in short cycles.
#### key ideas
1. continuous interation
2. automated testing
3. automated deployment

&nbsp;  

# requirements
Define a requirements specification
1. procss:
    - create high-level descriptions.
    - capture WHAT not the HOW of the solution.
2. product:
    - documentation.
    - or software requirement specification (SRS doc).  

Good requirements specification saves time and money.

## user requirements vs system specifications
1. requirements for the user, write in the user language.
2. specifications for the developer, write in the system language.
3. be sure that your specification meet the requirements.

### Example:  
He want to be able to put the boat on a rack by themselves.
- User requirement: 
    1. One person must be able to load the boat on the cat rack.
- System Specifications:  
    1. boat must be lighter than 100lb.
    2. boat must have handles.
    3. car rack must be padded for easily slides.
    4. etc.

## Non-functional requirements
1. very important
2. consider them separately from the functionality
3. consider on a case-by-case basis
### Example:  
1. system design constraints: like using a specific tool for designing
2. quality related constraints: like security, performance, and usability  
### classifications
1. product requirements: protocol, encodings, encryption, etc.
2. oranization requirements: company standards, code style, etc.
3. external requirements: government regulations, etc.

## WRSPM Model

![WRSPM](/WRSPM.png)
https://medium.com/@sofiia./wrspm-reference-model-or-the-world-machine-model-54f6436f31e7  
&nbsp;  

Must be careful of word assumptions,they are difficult to capture.
If the "W, S imply R" and "M, P imply S", the solution is right.


### Example: Patient Monitor  
1. World assumptions: a nurse can hear the buzzer
2. Requirements: when the patient's heart stops, a nurse shall be notified.
3. Specification: if the sound from the sensor falls below a  certain threshold, the buzzer shall be actuated,
4. Program: code.
5. Machine: hardware.


# Software Architecture
## practiacl definition
Partitioning large systems in to smaller ones that can be:  
1. created separately and operate individually.
2. have business value.
3. integrated with one another or with existing systems.

### a good architect pros:
1. helps organize the workforce and resources
2. allows for parallelization
3. helps build-or-buy decisions and funding

## Models
start from exist models, adjust them only if necessary
1. Pipe-and-Filter:  
Decompose a task that performs complex processing into a series of separate elements that can be reused. It's best suited for a system that includes several subsets of functionality that are used in more than one area of the system.  
https://learn.microsoft.com/en-us/azure/architecture/patterns/pipes-and-filters
2. Blackboard:  
One "Blackboard" shared data/processing across all compoents. It's best suited for a system that most important aspect is the shared data.  
https://cs.uwaterloo.ca/~m2nagapp/courses/CS446/1195/Arch_Design_Activity/Blackboard.pdf  
3. Layered:  
Sperating core element of the system into layses such that we can modify one layer without affecting others.
https://cs.uwaterloo.ca/~m2nagapp/courses/CS446/1195/Arch_Design_Activity/Layered.pdf  
4. Client-server:  
https://cs.uwaterloo.ca/~m2nagapp/courses/CS446/1195/Arch_Design_Activity/ClientServer.pdf  
5. Event-based:  
https://cs.uwaterloo.ca/~m2nagapp/courses/CS446/1195/Arch_Design_Activity/Event.pdf  

- Additional resources:  
UW Arch Design handouts
https://cs.uwaterloo.ca/~m2nagapp/courses/CS446/1195/Arch_Design_Activity/  
10 common software architectural  
https://towardsdatascience.com/10-common-software-architectural-patterns-in-a-nutshell-a0b47a1e9013  

## Design process
1. System structuring: How the system decomposed in to subsystems and the relationships between sub-systems.  
2. control modeling: How the software will work once it's running.
3. modular decomposition: Looking for resource management and quality attributes like reliability, security ect.

### Sub-systems: idependent system which holds business value.
### Module: component of a sub-system which cannot function as standalone systems.