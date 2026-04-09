# Feedback for All Groups - Product Thinking & Demo VINFAST_C5

## VINFAST_X1 (Car Purchase Consultation Chatbot)

**Problem-Solution Fit:** 5  
**AI Product Thinking:** 2  
**Demo Quality:** 5  

### What was done well
- The product addresses a real need. Buying a car is a major financial decision, so there is genuine demand for this solution.

### Areas for improvement
- Need more specific cost analysis (e.g., cost of calling YouTube review videos).
- Need more specific consultation on issues related to owning electric vehicles (e.g., information about charging station coverage near the user’s residence, comparison of usage costs for commercial purposes).
- Data does not yet include information from car brands outside the current manufacturer.
- High input sensitivity: When the sample car model in the input is changed to a different model, the chatbot fails to provide an answer.

---

## VINFAST_X2 (Vehicle Condition Diagnosis and Maintenance Scheduling)

**Problem-Solution Fit:** 2  
**AI Product Thinking:** 2  
**Demo Quality:** 3  

### What was done well
- Correctly identified the pain point, helping users save time in identifying vehicle errors and understanding the current condition of their car.
- Fast response time (2 seconds).
- Uses real-time sensor data, enabling better predictions.

### Areas for improvement
- What happens if the AI gives a wrong answer? Need a button to call a technician and implement a Human-in-the-loop mechanism.
- To avoid legal risks when the AI misses life-threatening errors, the system must apply a **"Fail-safe"** mechanism. When dangerous signs are detected, the AI Agent should automatically lose its processing rights and immediately switch to emergency human connection mode (to ensure absolute safety).
- Diagnosis needs to be presented in a way that is easily understandable to general users (for example, people who rarely use cars may not understand technical vehicle issues, so clear explanations are required).
- Vehicle problems may fall outside the scope of the sensors, yet users can still input them to the chatbot.

---

## VINFAST_C4 (EV Route Suggestion with Charging Station Stops)

**Problem-Solution Fit:** 1  
**AI Product Thinking:** 1  
**Demo Quality:** 2  

### What was done well
- Correctly identified the pain point and provided a solution direction.

### Areas for improvement
- Must define the problem more thoroughly, add user feedback, out-of-the-box queries, and increase logical reasoning.
- Need better control over LLM Hallucination as the AI easily generates incorrect information.
- Apply additional external conditions, such as battery degradation, to estimate travel distance more accurately.
- Need to check the status of charging stations, including how many slots are available or whether the station is under maintenance.

---

## X5 (Vinhomes Real Estate Recommendation)

**Problem-Solution Fit:** 3  
**AI Product Thinking:** 2  
**Demo Quality:** 4  

### What was done well
- Correctly identified a common pain point and provided strong support to thoroughly solve the time-consuming issue for both buyers and sellers during the information research phase.
- Good demo, beautiful interface, and fast response.

### Areas for improvement
- **Out-of-Scope Handling and Anti-Hallucination:** The system currently fails when users ask questions outside the defined scope. The team needs to implement a Guardrails layer to detect out-of-scope questions and respond gracefully (for example: “I only specialize in real estate consultation. May I help you find a house in another district instead of talking about the weather?”).
- **Optimize "Matching" Capability:** Instead of relying only on keyword search, the team should apply Vector Database / Semantic Search to handle vague requests. For example: When a customer asks for “a house for people who like quiet places,” the system should prioritize areas near parks or dead-end alleys rather than searching only by price and area.
- Immediately add a mechanism where the AI acts as a **"potential customer filter"**, then transfers the data to the sales consultant along with a summary of the customer’s preferences.