## Requirements
- Combinations of all possible cases. [Parwise testing](http://www.pairwise.org/)

## Libraries
- [Awesome dotnet](https://github.com/quozd/awesome-dotnet) - List of most popular libraries
- [Awesome dotnet core](https://github.com/thangchung/awesome-dotnet-core) - List of most popular libraries for Dot Net Core

## Technical features
- **Code comments** - write comments for classes, methods, etc. Generate documentation.
- **Code documentation** - write documentation (ex. README.MD files) about technical features "How log something", "How valdate data". Best practice is to reuse already implemented technical features, but without proper documentation it's hard to find out how some feature implemented. Write documentation with examples and link code implementation if possible. Describe used frameworks, libraries, patterns, etc.
- **Logging** - Implement as simple as possible. Collect logs by using popular library like NLog, lo4net and others. Review logs periodically or send daily/week reports. Consider send email for unhandled exceptions.
- **Validation** - each application has different types of validation. In ideal implementation validation in backend should be reused in frontend. Validation is one of the application's core functionalities. Define validation layer and reuse on all layers. Think about localisation of validation errors. Helpful questions: "How to display localised validation error at frontend for input field which returned by backend (backend has multiple layers and data containers can be different between layers (DTO, Entities, Business layer, Data layer, etc.)?"
- **Localisation** - many applications requires two or more languages. One of the problematic areas is to implement localisation for multiple layers/tiers. For example application has two projects: Web API back end + SPA frontend. In ideal situation backend and frontend are using the same source of translations and current localisation is synchronized between them.
- **Multi tenancy**
- **Web API. REST API vs RPC** - Clean ans simple implementation of Web Api (doesn't related to Net framework) is't easy task. Choose between two types of APIs. There is a lot of buzz around REST API, but also there are a lot of popular services which have RPC based API. One of the biggest disadvantages of REST API that it bad fits actions (ex. "Generate report action", "Move item", "Copy item").
  - [Understanding RPC Vs REST For HTTP APIs](https://www.smashingmagazine.com/2016/09/understanding-rest-and-rpc-for-http-apis/)
  - [Do you really know why you prefer REST over RPC?](https://apihandyman.io/do-you-really-know-why-you-prefer-rest-over-rpc/)
  - [Best Practices for Designing a Pragmatic RESTful API](https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api)
  - [https://developer.todoist.com/sync/v7/](https://developer.todoist.com/sync/v7/)
- **Open API + Swagger CodeGen** - Generate Api specification based on Open API specification. Generate code based on specification. For example generate protocol based on Web API and generate TypeScript/JavaScript client code based on protocol.
  - [https://www.openapis.org/](https://www.openapis.org/)
  - [https://swagger.io/swagger-codegen/](https://swagger.io/swagger-codegen/)
  - [https://medium.com/slack-developer-blog/standard-practice-slack-web-openapi-spec-daaad18c7f8](https://medium.com/slack-developer-blog/standard-practice-slack-web-openapi-spec-daaad18c7f8)
- **[Code contracts](https://docs.microsoft.com/en-us/dotnet/framework/debug-trace-profile/code-contracts)** - Additional info [http://deviq.com/guard-clause/](http://deviq.com/guard-clause/)
- **Code interception. AOP** - [https://msdn.microsoft.com/en-us/library/dn178466(v=pandp.30).aspx](https://msdn.microsoft.com/en-us/library/dn178466(v=pandp.30).aspx)

## Guidelines
- **Abstract DateTime** - implement DateTimeProvider for better testing
- **New is glue** - [https://ardalis.com/new-is-glue](https://ardalis.com/new-is-glue)
- **Do not use static methods and properties** - [http://deviq.com/static-cling/](http://deviq.com/static-cling/)
- **Designing with interfaces** - [(https://www.javaworld.com/article/2076841/core-java/designing-with-interfaces.amp.html](https://www.javaworld.com/article/2076841/core-java/designing-with-interfaces.amp.html)**
- **Code control flow**
- **Reduce code nesting** - [https://refactoring.guru/replace-nested-conditional-with-guard-clauses](https://refactoring.guru/replace-nested-conditional-with-guard-clauses)
- **С# immutable parameters** - Do not change parameters inside method body. Functional programming.
- **Code cyclomatic complexity**

## Solution and projects structure
- [Architecting Modern Web Applications with ASP.NET Core and Azure eBook](https://aka.ms/webappebook) + [Sample ASP.NET Core reference application](https://github.com/dotnet-architecture/eShopOnWeb)
- **Use namespaces over projects**
  - [https://lostechies.com/chadmyers/2008/07/16/project-anti-pattern-many-projects-in-a-visual-studio-solution-file/](https://lostechies.com/chadmyers/2008/07/16/project-anti-pattern-many-projects-in-a-visual-studio-solution-file/)
  - [https://codurance.com/2015/03/23/multiple-projects-in-visual-studio/](https://codurance.com/2015/03/23/multiple-projects-in-visual-studio/)
  - [https://ayende.com/blog/3158/the-two-project-solution](https://ayende.com/blog/3158/the-two-project-solution)
  - [http://geekswithblogs.net/FrostRed/archive/2008/10/03/125628.aspx](http://geekswithblogs.net/FrostRed/archive/2008/10/03/125628.aspx)
  - [http://codebetter.com/jeremymiller/2008/09/30/separate-assemblies-loose-coupling/](http://codebetter.com/jeremymiller/2008/09/30/separate-assemblies-loose-coupling/)
  - [http://www.hanselman.com/blog/AssemblyFiefdomsWhatsTheRightNumberOfAssembliesLibraries.aspx](http://www.hanselman.com/blog/AssemblyFiefdomsWhatsTheRightNumberOfAssembliesLibraries.aspx)
  - [https://msdn.microsoft.com/en-us/library/ee658109.aspx](https://msdn.microsoft.com/en-us/library/ee658109.aspx)
  
## Patterns
- **[Repository + Unit of Work + Specification](https://docs.microsoft.com/en-us/dotnet/standard/microservices-architecture/microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design)**
  - [Specification pattern](http://deviq.com/specification-pattern/)
  - [Implementing the Repository and Unit of Work Patterns in an ASP.NET MVC Application](https://docs.microsoft.com/en-us/aspnet/mvc/overview/older-versions/getting-started-with-ef-5-using-mvc-4/implementing-the-repository-and-unit-of-work-patterns-in-an-asp-net-mvc-application)

