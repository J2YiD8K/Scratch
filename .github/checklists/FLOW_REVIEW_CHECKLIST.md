# ✅ Power Automate Flow Review Checklist

<details>
<summary>🔁 Flow Design and Modularity</summary>

- [ ] Flow is modular and reusable across environments  
- [ ] Trigger type is appropriate and scoped correctly  
- [ ] Connection references used instead of direct connections  
- [ ] Parent-child flow architecture used where appropriate  
- [ ] Flow logic avoids excessive nesting or branching  
- [ ] Expressions and conditions are readable and documented  
- [ ] Avoids hardcoded GUIDs, URLs, or environment-specific values  

</details>

<details>
<summary>🧪 Testing and Error Handling</summary>

- [ ] Flow tested with edge cases and failure paths  
- [ ] Retry policies configured where needed  
- [ ] Error handling implemented using `Configure Run After` or `Scope` blocks  
- [ ] Flow handles nulls, empty arrays, and missing attributes gracefully  
- [ ] Flow includes fallback logic or notifications for critical failures  

</details>

<details>
<summary>📦 Solution Awareness</summary>

- [ ] Flow is part of a managed solution  
- [ ] Environment variables used for configurable values  
- [ ] Secure inputs/outputs enabled for sensitive data  
- [ ] Flow name and description are clear and traceable  
- [ ] Flow avoids deprecated actions or connectors  
- [ ] Flow uses Dataverse connector (not legacy CDS)  

</details>

<details>
<summary>🔗 Integration with Plugins and D365</summary>

- [ ] Flow triggers aligned with plugin logic and entity events  
- [ ] Flow avoids race conditions with plugin execution  
- [ ] Flow respects plugin depth and avoids triggering loops  
- [ ] Flow uses alternate keys or GUIDs consistently  
- [ ] Flow avoids redundant updates that could retrigger plugins  

</details>