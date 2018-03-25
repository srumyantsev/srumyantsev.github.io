## Requirements
- Combinations of all possible cases. [Parwise testing](http://www.pairwise.org/)

## Libraries
- [Awesome dotnet](https://github.com/quozd/awesome-dotnet) - List of most popular libraries
- [Awesome dotnet core](https://github.com/thangchung/awesome-dotnet-core) - List of most popular libraries for Dot Net Core

## Technical features
- **Code comments** - write comments for classes, methods, etc. Generate documentation.
- **Code documentation** - write documentation (ex. README.MD files) about technical features "How log something", "How valdate data". Best practice is to reuse already implemented technical features, but without proper documentation it's hard to find out how some feature implemented. Write documentation with examples and link code implementation if possible. Describe used frameworks, libraries, patterns, etc.
- **Logging** - Implement as simple as possible. Collect logs by using popular library like NLog, lo4net and others. Review logs periodically or send daily/week reports. Consider send email for unhandled exceptions.
- **Validation** - 
- **Localisation** - 
- **Open API + Swagger** - Generate Api based on Open API specification. Generate code based on specification. For example generate protocol based on Web API and generate TypesScript/JavaScript client code based on protocol.
- **[Code contracts](https://docs.microsoft.com/en-us/dotnet/framework/debug-trace-profile/code-contracts)**

## Guidelines
- **Abstract DateTime** - implement DateTimeProvider for better testing
- **New is glue** - [https://ardalis.com/new-is-glue](https://ardalis.com/new-is-glue)
- **Do not use static methods and properties** - [http://deviq.com/static-cling/](http://deviq.com/static-cling/)

## Solution and projects structure
[Architecting Modern Web Applications with ASP.NET Core and Azure eBook](https://aka.ms/webappebook) + [Sample ASP.NET Core reference application](https://github.com/dotnet-architecture/eShopOnWeb)
