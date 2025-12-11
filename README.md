# RBAC-for-conversational-systems

In modern conversational systems (GenAI chatbots), service requests expressed in natural language must be interpreted to identify the resource a user is trying to access and the action they intend to perform. The solution takes a user query and an access token (from Amazon Cognito), extracts the intended action and resource using an LLM, and evaluates the request using Amazon Verified Permissions (AVP). AVP, with Cognito as the identity source and Cedar-based policy definitions, ensures that authorization decisions are enforced consistently and centrally. Developers can integrate this into their GenAI applications to streamline compliance and deliver secure conversational experiences. 

In UI-based systems, resources and actions are well-defined through buttons, forms, and APIs, making it straightforward to enforce RBAC. In LLM-based chatbots, the same information is buried in unstructured natural language, creating the challenge of accurately extracting intent before authorization can even happen. Our solution is designed to address this challenge. 

This solution combines LLM-powered intent extraction with enterprise-grade access control to securing natural language interfaces. It converts user queries into structured action-resource pairs, which are evaluated against fine-grained Cedar policies using Amazon Verified Permissions (AVP). With built-in integration to Amazon Cognito, user identities are seamlessly authenticated via access tokens and mapped directly to authorization logic, ensuring secure and compliant access to backend services. 

##Key highlights:  

LLM-powered Action-Resource Extraction: Translates free-form user queries into structured action-resource pairs for accurate enforcement.  

Fine-Grained Access Control with Cedar + AVP: Secure every API or data interaction with policy-based authorization tied to roles, hierarchies, and relationships.  

Seamless Auth Integration with Cognito: Leverages the user's access token to map identity directly to permission logic, reducing friction and improving compliance.  
