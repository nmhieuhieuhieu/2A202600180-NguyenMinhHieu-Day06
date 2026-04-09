# Research Notes

## 1. Self-Troubleshooting Simple Issues for VinFast Electric Vehicles

**Focus:** Helping users resolve common minor issues on VinFast VF e34, VF e36, VF8, and VF9 without immediately visiting a service center.

### 1.1. "12V Battery Low" or Car Won't Start
- **Cause:** Weak 12V auxiliary battery (not the high-voltage traction battery).
- **Self-fix steps:**
  1. Park in a safe location.
  2. Open the hood and charge the 12V battery using a smart charger (2A–5A) for 20–40 minutes.
  3. Restart the vehicle.
- **Escalation:** If the issue persists after two attempts, contact a technician.

### 1.2. Low High-Voltage Battery / Range Anxiety
- **Self-fix steps:**
  1. Check battery percentage on the VinFast app.
  2. Switch to Eco mode and turn off air conditioning if necessary.
  3. Locate the nearest charging station via the built-in VinFast navigation.
- **Note:** Real-world battery degradation is typically 8–12% after 2 years. AI should factor this in for accurate range estimation.

### 1.3. Vehicle Not Charging (AC/DC)
- **Self-fix steps:**
  1. Clean the charging port if dirty.
  2. Try using the spare charging cable.
  3. Restart the vehicle (press start button twice without pressing brake).
  4. Check for error messages in the VinFast app.

### 1.4. Warning Lights on Dashboard (Regen, TPMS, Software Glitch)
- **Self-fix steps:**
  1. Take a screenshot of the warning.
  2. Fully power off the vehicle (disconnect 12V for 1 minute).
  3. Perform OTA software update via the VinFast app.
- **Safety note:** Never attempt to intervene in the high-voltage system.

### 1.5. Weak or Warm Air Conditioning
- **Self-fix steps:**
  1. Switch between Eco and Comfort modes.
  2. Clean the cabin air filter (easily accessible under the driver’s seat).
  3. Allow 2–3 minutes after startup for pre-conditioning.

## 2. Role of AI Chatbot in Self-Troubleshooting
- Provide clear, step-by-step instructions suitable for non-technical users.
- Always include a “Call Technician Now” button (Human-in-the-loop).
- Automatically trigger **Fail-safe** mode and escalate to human support when dangerous symptoms are detected (burning smell, high temperature, brake issues, airbag warning).

## 3. VinFast Real-World Data & References
- Official VinFast VF series user manuals (2024–2025).
- Community insights from “VinFast Owners Club” Facebook group.
- Battery degradation studies: average 8–10% capacity loss after 2 years in Vietnam conditions.
- Charging infrastructure: Over 150,000 charging ports nationwide as of 2026.

## 4. Study on LangRAG and AI Agent Architectures

### 4.1. Retrieval-Augmented Generation (RAG) Architecture
RAG combines **retrieval** of relevant external documents with **generation** by Large Language Models to produce more accurate and up-to-date responses.

**Core Components:**
- **Retriever**: Converts user query into embeddings and performs semantic search in a Vector Database.
- **Augmentor**: Combines the original query with retrieved documents to create enriched context.
- **Generator**: LLM generates the final answer based on the augmented prompt.

**Benefits for our projects:**
- Significantly reduces hallucination.
- Enables use of real-time or domain-specific data (VinFast car specs, charging station status, real estate listings).
- Easy to update knowledge without retraining the model.

**Advanced variants:** Modular RAG, LongRAG (using larger retrieval units for longer context).

### 4.2. AI Agent Architecture with LangGraph
**LangGraph** (part of the LangChain ecosystem) is a framework for building reliable, stateful, and controllable **AI Agents** using graph-based workflows.

**Key Concepts:**
- **State**: Shared memory that persists across steps (conversation history, intermediate data, user preferences).
- **Nodes**: Individual actions or tools (e.g., Retrieve, Diagnose, Decide, Call Human).
- **Edges**: Connections between nodes, including **conditional edges** that route the flow based on LLM decisions.

**Advantages of LangGraph:**
- Better support for multi-turn conversations and complex logic.
- Enables **Human-in-the-loop**, persistence, streaming, and easy debugging.
- Ideal for building **multi-agent** systems where specialized agents collaborate.

**Application to Our Projects:**
- **X2 (Diagnosis)**: Build an agent with a Fail-safe node that automatically escalates critical errors to a human.
- **X1 & C4**: Agent can call tools to fetch car data, calculate routes (including battery degradation), and check charging station availability.
- **X5 (Real Estate)**: Multi-agent workflow — one agent collects preferences, another filters properties, and a final agent summarizes and transfers qualified leads to sales consultants.
- **RAG + LangGraph Combination**: RAG provides accurate data retrieval while LangGraph handles reasoning, tool calling, and decision-making.

**Recommendation:**
- Use LangGraph to create structured, safe, and extensible agent workflows.
- Combine with Vector Databases (e.g., FAISS, Chroma, Pinecone) for powerful semantic search.
- Add a Guardrails layer to handle out-of-scope queries reliably.

**References:**
- LangChain & LangGraph official documentation.
- Research papers on RAG and agentic AI systems.
- Best practices for safety-critical AI applications.

**Conclusion:** Understanding RAG and LangGraph architectures allows us to build AI solutions that are not only intelligent but also **safe, reliable, and scalable** — especially important for EV-related and diagnostic applications.