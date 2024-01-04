# Assignment Topic:

As a software development professional, you will run into all kinds of projects and situations within those projects. This assignment is designed to present you with a fictitious situation and ask you to recommend a software development approach suited to the situation.  

# Here is the situation: 

Zenith Healthcare is a new company in the market and has launched its product two years ago. The product is loved by clients and is growing in popularity.  The level of product demand was not anticipated, and the current system architecture cannot support the rising demand. To support the anticipated demand, the company needs to re-architect the system and provide the exact same functionality.  Thus, the requirements from the client perspective are very well known and do not need to change.  What needs to be changed in the system to support the growing demand is also well understood.  The product has 4, fairly independent components.   All 4 components need to be re-architected.  Out of the 4, one of them has caused the most pain and the organization could benefit greatly if that component could be replaced first with a new, highly scalable architecture. The work of migrating to a new platform is a tedious job and the deployment of a new system will involve a lot of external communication, managing customer expectations, etc.

The technical architect and one project manager will be working from the corporate headquarters in Germany, but most of the team who will be doing the coding for the migration will be offshore in Belarus. The testing team will also be in Belarus.

## What software development methodology would you suggest for this situation and why? 

### analyzing
1. The requirements do not need to change. What needs to be changed (architect) is well understood.
    - know the problem and solution except for the scale.
2. four components, the organization could benefit greatly if one specific component could be replaced first.
    - benefits from deploying part of the project early.
3. will involve a lot of different people.
    - roll the project out incrementally to get some feedback.
4. developer are in different countries.
    - benefit from separate phases clearly.

### suggestion
- I suggest the incremental waterfall model, because:
    1. requirements are clear and less concerned about rework.
    2. Architect and PM can finish the first two phases of the waterfall model and then hand it to the coding team in another country.
    3. It can deliver value earlier by working on one component first.
    4. It can get feedback and make changes between increments.


## Imagine that you were the lead or project manager for this project. For the selected model, take us through a simulated/fictitious journey on how this project will be completed all the way from defining requirements to deployment.

- gate 1: Establishing business case.
1. requirements: Defining the requirement. Evaluate it for feasibility, schedule, and cost. Make sure the client's needs are satisfied. 
2. design: Designing the first increment for the components that the organization could benefit greatly. May consider integration and focus on architect scalability.
- gate 2: Make sure the design is clear and can be implemented, hand it to the coding team in another country, and continue working on the early stage of the second increment.
3. implementation: Make sure the code is following the document. Keep communication with the design team.
4. testing: May focus on integration between components. Try to scale up the product to make sure the scalability can satisfy future demand.
- gate 3: Making sure the product is validated and ready to deploy.
5. deploy: Having a practical rollback plan.
6. gather feedback to see if any changes need to be done before the second increment.
7. repeat until all four components are re-architected.

## Assume that you are the quality lead or technical lead on this project. What kind of testing would you suggest the team to do? Be sure to justify your answer. To answer this question, first, list down the key things from the use case above that are really important. After that, identify what type of testing would you want the team to do to make sure that upgraded product is high quality and deployed defect free.
1. scalability: white-box
2. safety: white-box and black-box
3. reliability: white-box and black-box
4. integration between components: white-box
5. performance: white-box and black-box
6. usability: black-box


## Continuing your role as a quality lead or technical lead for the project. Write a few examples of test cases or a descriptive narrative for what you expect the testing team to use when testing this product.
1. scalability: Scale up to access hundred times of demand.
2. safety: Make sure users can not access the information without authorization.
3. reliability: Run it in the non-production environment for a week with hundred times of demand.
4. integration Between components: four components can work together without errors.
5. performance: Checking algorithm and Big O notation. Make sure it can access through an older system.
6. usability: users can use the product from the beginning to the end without extra information