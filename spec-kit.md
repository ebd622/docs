# Spec-kit: HowTo

## Mostly used commands
Check and Upgrade version
```
specify version
specify self upgrade --dry-run
```
Init spec-kit for the (current) project
```
specify init .
```
This will also create an empty constitution.md (from a template)

## Standard workflow
Constitution → Specify → Clarify → Plan → Tasks → Implement → Converge
### Constitution
```
/speckit-constitution
/skill:speckit-constitution
```
Example:
```
/skill:speckit-constitution
- Java 21 LTS is mandatory.
- Use the latest stable Spring Boot version.
- Maven is the standard build tool.
- Follow REST API best practices and OpenAPI 3 documentation.
- Use PostgreSQL as the primary database.
- Use JUnit 5, Mockito, and Testcontainers for testing.
- Use feature-based package structure.
- Use Java Records for DTOs where appropriate.
- Implement input validation using Jakarta Validation.
- Use Spring Boot Actuator and Micrometer for observability.
- Provide Docker support.
- Use secure coding practices, externalized configuration, and no hard-coded secrets.
- Prefer clean code, SOLID principles, and maintainable architecture.
- Require API versioning and standardized error responses.
- Define governance, compliance, and amendment rules for the constitution.
```
It is also possible to specify some particular details for constitution. For example
```
/skill:speckit-constitution
jackson2 is deplicated. Jackson3 should be used in all new implementations
```

### Specify
TODO
### Clarify
TODO
### Plan
TODO
### Tasks
TODO


# Resources
* SDD
  * [Spec Driven Develppment](https://youtu.be/RhaF4LVAVng?si=3nu51beWxWgMGXtL) (example with supadata.ai)
* Spec-kit
  * [GitHub Spec-Kit](https://github.com/github/spec-kit)
  * [Extentions](https://speckit-community.github.io/extensions)
