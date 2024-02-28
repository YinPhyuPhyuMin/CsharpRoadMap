# CsharpRoadMap
YouTube Link [(https://www.youtube.com/watch?v=1Lcr2c3MVF4&list=PLYpjLpq5ZDGstQ5afRz-34o_0dexr1RGa&index=3)]

# Clean Architecture .Net 6

There are 4 layers in Clean Architecture.
1. Domain Layer - Entities -(Can not reference the other layer)
2. Application Layer - Business Logic (Service Layer, (CQRS pattern, Domain Driven are put in Command Handler and Query Handler)) - (can reference the Domain Layer)
3. Infrastructure Layer - Database Access and Data Access Repository, email storage, message blocker queue logic (Can reference the Application Layer, Cannot reference the Presentation Layer)
4. Presentation Layer - API, endpoints (Can reference the Application Layer, Cannot reference the Application Layer)

# Architecture Test
1. DomainShouldNotHaveDependencyOnOtherProjects (Application,Infrastructure,Presentation)
2. ApplicationShouldNotHaveDependencyOnOtherProjects (Infrastructure, Presentation)
3. InfrastructureShouldNotHaveDependencyOnOtherProjects (Presentation)
4. PresentationShouldNotHaveDependencyOnOtherProjects (Infrastructure)
5. CommandHandlerShouldHaveDependencyOnDomain
6. ControllerShouldHaveDependencyOnMediatorR
   * MediatorR - Library,Sending Our Commands and query Objects to their respective handlers

# Domain Driven Architecture
 Use the Domain Driven Architecture in Domain Layer's Entity Class.

 * Code Refactoring the Business Logic from Command Handler, Query Handlder in Application Layer to Domain Layer's Entity Class.

 We bind the data in Entity Constructor.
 We need to change the Constructor (internal) and property (private setter) because we cannot change the value from outer.
