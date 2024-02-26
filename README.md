# CsharpRoadMap
Clean Architecture .Net 6
++++++++++++++++++++++++++
There are 4 layers in Clean Architecture.
1. Domain Layer - Entities -(Can not reference the other layer)
2. Application Layer - Business Logic (Service Layer) - (can reference the Domain Layer)
3. Infrastructure Layer - Database Access and Data Access Repository (Can reference the Application Layer, Cannot reference the Presentation Layer)
4. Presentation Layer - API, endpoints (Can reference the Application Layer, Cannot reference the Application Layer)
