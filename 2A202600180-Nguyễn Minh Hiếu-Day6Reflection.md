# Individual Reflection

**Name:** Nguyen Minh Hieu

**Student ID:** 2A202600180 

**Project:** VinFast Smart Rescue Orchestrator

## 1.Specific Role
I was responsible for the **ROI Analysis** and the **Mini AI Spec** for our project. My focus was on the strategic planning and ensuring the product had a clear path to business value.

## 2. Specific Contributions
* **ROI Analysis & Mini AI Spec:** I authored Section 5 (ROI 3 scenarios) and Section 6 (Mini AI Spec) of the final documentation. This included defining the Conservative, Realistic, and Optimistic financial outlooks and setting the "Kill Criteria."

* **Workflow Construction:** I contribute to the design of the operational workflow, mapping out how the AI orchestrates the journey from an initial incident alert to the final rescue dispatch.

* **Mock Data Generation:** I built the foundational mock dataset covering basic vehicle incidents (e.g., dead batteries, tire issues, software glitches) to ensure the prototype had realistic inputs to process.

* **Peer Feedback Member:** I served as a evaluator for our team during the Gallery Walk, observing and writing detailed feedback forms for other teams in our zone.

## 3. SPEC Strengths/Weaknesses
* **Strongest:** **ROI Analysis**. By grounding the AI features in concrete financial scenarios, I was able to clearly demonstrate how the "Smart Rescue Orchestrator" would actually save costs and improve customer retention.

* **Weakest:** **User Stories 4 Paths**. We initially struggled to define the "Failure" and "Correction" paths for rare rescue edge cases, which required several iterations to make them realistic.

## 4. Other Contributions
* **Peer Reviewing:** I visited multiple teams in the zone, listened to their demos, and provided constructive scores and feedback on their Problem-solution fit and AI thinking.

* **Workflow Refinement:** I worked closely with the team to ensure the "Automation vs. Augmentation" logic was consistent across both the Spec and the actual Demo.

## 5. One thing learned

I learned the practical importance of the **Threshold** concept in AI products. Specifically, I realized that in a high-stakes field like vehicle rescue, the AI must have a very low threshold for handing off to a human operator when safety is involved.

## 6. What would I change?

If I were to redo this project, I would focus on the following technical and strategic improvements to move the product beyond a basic prototype:

* **Refine Pricing Accuracy and Metrics:** I would improve the cost estimation logic, as guessing prices is currently difficult without specific metrics. Providing estimates that are significantly lower than reality could lead to user dissatisfaction and loss of trust in the VinFast service.
* **Implement 2FA for Emergency Vehicle Access:** I would integrate a Two-Factor Authentication (2FA) system specifically for "locked-out" scenarios. This would allow users to verify their identity quickly and unlock their vehicle doors directly through the app during an emergency.
* **Develop a Robust RAG System:** I would implement a clear Retrieval-Augmented Generation (RAG) architecture to ensure the AI provides accurate, manual-based technical advice rather than relying on general knowledge.
* **Human-in-the-Loop Integration:** I would add a dedicated "Call Operator" button or an intent-recognition feature that allows users to instantly connect with a human consultant when the AI reaches a low-confidence threshold or when a user specifically requests it.
* **Speech-to-Text (STT) Integration:** I would implement STT capabilities to allow users to interact with the rescue orchestrator hands-free. This is critical for safety, enabling drivers to report issues or request help without taking their eyes off the road.
## 7. AI Utility & Limitations
* **Pros:** AI was extremely helpful in brainstorming the different cost-saving variables for the ROI scenarios and drafting the initial structured content for the Mini AI Spec.

* **AI misleading (Cons):** AI occasionally suggested rescue procedures that were technically inaccurate for Electric Vehicles (EVs), which required me to manually audit and correct the mock data to align with VinFast's actual technology.