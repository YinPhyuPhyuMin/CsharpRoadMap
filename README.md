# CsharpRoadMap
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
 It is include in Application Layer. In Commmand and Query Handler, we use CQRS patterns with Domain Driven.
 We bind the data in Entity Constructor.
