# ✅ Code Review Checklist for D365 Plugin Development

<details>
<summary>🧠 Plugin Architecture and Execution</summary>

- [ ] Follows DRY and SRP principles  
- [ ] Plugin base class used for shared context/service access  
- [ ] Plugin class delegates to service layer or handler  
- [ ] No logic in constructors
- [ ] Plugin logic is idempotent and safe for re-execution  
- [ ] Depth check used to prevent recursion or infinite loops  
- [ ] Uses `InvalidPluginExecutionException` and `OrganizationServiceFault` correctly  
- [ ] Uses Tracing Service where appropriate  
- [ ] Plugins registered at the correct stage  
- [ ] Plugins return at the earliest opportunity  

</details>

<details>
<summary>🔍 Query and Data Access</summary>

- [ ] `QueryExpression` used consistently  
- [ ] Queries use restricted column sets, lookup filters, and active state  
- [ ] Avoids `AllColumns = true` and over-fetching  
- [ ] Input parameters validated and null-checked  
- [ ] Handles `EntityImage` and `Pre/Post` safely  
- [ ] Avoids direct use of `ExecuteMultipleRequest` unless explicitly needed  

</details>

<details>
<summary>🔒 Security and Data Integrity</summary>

- [ ] Sensitive data not logged in TracingService  
- [ ] Plugin respects impersonation and user privileges  
- [ ] Entity state transitions validated  
- [ ] No hardcoded values or magic numbers  

</details>

<details>
<summary>🧩 Modularity and Reusability</summary>

- [ ] Shared logic extracted into helpers or services  
- [ ] Metadata-driven logic used where applicable  
- [ ] Common constants and enums centralized  
- [ ] Logging and exception handling abstracted  
- [ ] Plugin logic decoupled from Power Automate triggers  

</details>

<details>
<summary>🧪 Testing and Coverage</summary>

- [ ] Unit tests mock `IOrganizationService`, `ITracingService`, and `IPluginExecutionContext`  
- [ ] Edge cases and exception paths covered  
- [ ] Tests validate both success and failure scenarios  
- [ ] Test data uses early-bound entities and avoids magic strings  

</details>

<details>
<summary>🎨 Code Style and Documentation</summary>

- [ ] XML Summary tags used for public methods  
- [ ] Consistent naming conventions (PascalCase for classes, camelCase for variables)  
- [ ] Regions used sparingly  
- [ ] No commented-out code in production  

</details>

<details>
<summary>🧑‍💻 TypeScript Web Resource Standards</summary>

- [ ] Uses repository pattern for data access abstraction  
- [ ] Business logic separated from UI and data layers  
- [ ] Interfaces used for models and services  
- [ ] Promises and async/await used consistently  
- [ ] Avoids direct DOM manipulation — uses framework or abstraction  
- [ ] Type safety enforced with strict types and enums  
- [ ] Web resources are modular and reusable across forms  
- [ ] Logging and error handling abstracted into shared utilities  
- [ ] Code compiled and bundled cleanly for deployment  

</details>