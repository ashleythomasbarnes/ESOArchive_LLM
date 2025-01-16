# README

This repository is designed to test how different Large Language Models (LLMs) respond to the following prompt:

> **Could you give a quick walk-through of how I could upload my MUSE data to the ESO archive?**

---

## Results 

Currently tested the followng, with responses in the following directories: 

```
responses/
  chatgpt-o1.md # ChatGPT-o1 with no additional support
  dmo.md # The Digital Support Astronomer
  ...
```

And the results are: 

| LLM          | Mentioned Phase 3? | Provided Directory Structure? | Provided References? |
|--------------|--------------------|-------------------------------|-----------------------|
| chatgpt-o    | Yes                | Yes                           | Yes (ESO links- but incorrect)       |
| DMO          | No                | No                          | No                  |


---
## Workflow 

Below is the workflow for testing and comparing responses from various LLMs.

### 1. Purpose

The aim is to evaluate how effectively each model:
1. Understands the **MUSE data submission** context.
2. Provides a **step-by-step** guide or outline for uploading data to the **ESO Phase 3** system.
3. Complies with **official requirements** (e.g., data format, naming conventions, metadata completeness, etc.).

By comparing responses, we can gauge the models’ accuracy, clarity, and overall usefulness.

---

### 2. Setup

To get started:

1. **Clone this Repository**  
   ```bash
   git clone https://github.com/your-username/muse-eso-archive-LLM-tests.git
   cd muse-eso-archive-LLM-tests

	2.	Prepare Your LLM Testing Environment
	•	You can use an online chat interface (ChatGPT, Bard, Claude, etc.) or a locally hosted LLM (e.g., Llama, GPT-Neo, etc.).
	•	Ensure you have any necessary API keys if you’re testing via an API.
	3.	Read the Prompt Carefully
Make sure to submit the exact prompt (below) to each LLM. Consistency is crucial.

3. The Prompt

``
    Could you give a quick walk-through of how I could upload my MUSE data to the ESO archive?
``

4. Testing Procedure
	1.	Submit the Prompt: Paste the exact prompt into the LLM interface or make an API request with the prompt text.
	2.	Record the Response: Copy the response into a text file or Markdown file within this repository (e.g., responses/llm_name.md).
    3.	Compare Responses (TODO): Create a comparison table or notes highlighting differences in thoroughness, correctness, or style:


5. Analysis & Conclusions
    
    After collecting the responses:
	1.	Evaluate Accuracy: Check if the steps align with the MUSE Phase 3 official documentation.
	2.	Assess Completeness: Are any steps missing (e.g., data verification, flux calibration details)?
	3.	Note Potential Misinterpretations: Some LLMs might hallucinate steps or make assumptions not found in official guidelines.

Use these insights to determine which LLM offers the most reliable and clear instructions for uploading MUSE data to the ESO archive.

---
## License

This project is licensed under the MIT License. Feel free to fork, modify, and share your results.