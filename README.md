# Guide to Vijil.ai's LLM Evaluations

## 1.	Building Trustworthy AI Agents for the Enterprise

In an era where AI systems are becoming integral to business operations, ensuring their reliability and trustworthiness is critical. This is the mission of Vijil.ai, a Menlo Park-based startup, which recently emerged from stealth mode with $6 million in seed funding from Mayfield’s AI Start fund and Google’s Gradient Ventures. Led by Vin Sharma and a team of engineering leaders from AWS who previously built large-scale AI systems like Amazon SageMaker and Bedrock, Vijil.ai is focused on addressing a fundamental problem: how to build and deploy AI agents that enterprises can trust.

## 2.	The Challenge: Trust and Reliability in AI

Generative AI, especially in large language models (LLMs), has become a cornerstone of innovation across various industries. However, the potential risks associated with these AI systems—such as biased outputs, data breaches, and unreliable behavior—have created hesitation among businesses to deploy them at scale. In some well-known cases, AI agents have produced misleading or erroneous outputs, putting organizations’ reputations and revenue at risk.

Traditional methods to evaluate AI trustworthiness, like relying on external consultants, AI benchmarks, or “vibe checks,” are inadequate and inefficient for large-scale AI deployment. Enterprises need a robust way to measure the trustworthiness of their AI systems, particularly in the context of privacy, security, and compliance.

## 3.	Vijil’s Solution: Measuring and Improving AI Trustworthiness

Vijil aims to solve this problem by offering a cloud-based platform that evaluates AI agents based on their specific business contexts. The platform automatically generates a comprehensive test suite using just a few data samples from each customer. This test suite assesses the performance, reliability, privacy, and security of the AI model in real-world scenarios. The platform also provides a “defense-in-depth” strategy to mitigate any detected risks, including a perimeter defense mechanism that rapidly identifies malicious prompts and unsafe responses.

One of Vijil’s key differentiators is its ability to scale trust evaluations. The company’s Vijil Evaluate service runs over 1.5 million tests, executing them 100 times faster than traditional alternatives. Meanwhile, the Vijil Dome product offers real-time, adaptive defense against errors and attacks, continuously learning from usage to improve detection accuracy.

## 4.	More on Vijil’s Evaluation Framework

Vijil’s evaluation service is built on four key components: detectors, probes, scenarios, and harnesses.

<img width="273" alt="image" src="https://github.com/user-attachments/assets/1e45022d-8531-4bd4-a11b-7850b6c6eaf0">

 
At the lowest level, detectors scan model outputs for undesirable features, like identifying fake Python packages. If such features are detected, they register as successful attacks on the model. 

Next, probes are sets of prompts designed to elicit specific undesirable responses, such as those linked to malware. 

Scenarios consist of collections of probes with a common goal, aimed at targeting specific vulnerabilities in the model. 

At the top level, harnesses combine one or more scenarios to generate an overall evaluation report or trust score. 

To evaluate a model on the Vijil platform, users select one or more harnesses, which may represent different dimensions of evaluation. For more detailed insights and diagrams, users can refer to Vijil’s documentation.

This system ensures thorough model evaluation across various levels of risk and performance metrics.

## 5.	Evaluating LLM Models Using the Vijil Platform: A Step-by-Step Guide

Vijil provides a comprehensive platform to evaluate the performance of Large Language Models (LLMs) by focusing on various dimensions as below:

•	Security
•	Privacy
•	Hallucination
•	Robustness
•	Toxicity
•	Stereotype
•	Fairness
•	Ethics

Here is a step-by-step guide to help you get started:

5.1 Create an Account and Access the Platform
Navigate to https://score.vijil.ai/ and sign up for an account. After verifying the account creation, contact the team for access. 

      <img width="90" alt="image" src="https://github.com/user-attachments/assets/65635dac-a622-429c-9ce5-420c98a42972">


After the user have been granted access, successful login takes the user to
the homepage as shown below:

<img width="365" alt="image" src="https://github.com/user-attachments/assets/e0d5bc10-e76a-4ad0-b35b-7d4ae4e98ecb">

     


5.2 Creating Evaluations
Vijil offers evaluations of both popular prebuilt models as well 	custom models. 

5.2.1 Select a Model

Currently it supports the following models hubs:

OpenAI 
gpt-4o, gpt-4-mini, gpt-4-turbo, gpt-4, gpt-3.5-turbo, 
gpt-3.5-trubo-16k, gpt-3.5-turbo-instruct

Together
The platform hosts numerous models from llama family, 	
Mistral family, Qwen family of models and others including:

meta-llama/Meta-Llama-3.2-405B-Instruct-Turbo, 
meta-llama/Meta-Llama-3.1-70B-Instruct-Turbo
Qwen/Qwen 1.5  - 110B-Chat 
mistralai/Mistral-7B-Instruct-v0.3
NousResearch/Nous-Hermes-2-Mistral-7B-DPO

OctoAI
Wizardlm-2-8x22b, mixtral-8x22b-instruct

Vertex
google/gemini-1.5-pro-001, google/gemini-1.5-flash-001

5.2.2 Selecting an API Key

Running evaluations requires generating response using the preselect LLM. The user needs to store the relevant API key in the API section https://score.vijil.ai/api_token. Once the API Key is stored, they can select the API Key while creating the evaluation.

5.3. Select Evaluation Criteria 
Vijil focuses on several evaluation dimensions and scenarios.

5.3.1 Select Evaluation modes: Full or Lite
Vijil.ai offers flexible both running full and lite evaluations. Running “Lite” mode offers a cheaper and faster evaluation across all or selected dimensions. 

5.3.2 Selecting dimensions/scenarios
User can select one or more dimensions from the menu.

5.3.3. Evaluation Scenario
Each dimension consists of one or more scenario. For example, Fairness dimension consists of three scenarios: Question Answering Bias, Gender Income Bias, Professional Bias. Here is a view of Evaluations tab taken from https://score.vijil.ai/evaluations/create-evaluation

        
  <img width="435" alt="image" src="https://github.com/user-attachments/assets/a52d0f67-83f7-47cb-adba-610295e00bef">
        

Once all the parameters are selected, user can go ahead and create the evaluations. Depending on selected parameters, it can take from few seconds to few minutes to complete the evaluation. User can also track the evaluations progress while its running.

5.4 Analyzing Evaluation Results
Upon completion of evaluation, user can see the evaluation report as below. Here I only ran the evaluation for dimensions Privacy, Hallucination, Performance, and Ethics dimensions. 

<img width="468" alt="image" src="https://github.com/user-attachments/assets/0d380313-7a1a-4698-aaf9-bc2f242df58d">

 
5.4.1 Evaluations deep dive
One can go in details of each dimension, scenario, questions, and LLMs response to gain deeper insights into evaluations from the report as shown below. Use this feedback to iteratively improve your model’s performance.

 <img width="363" alt="image" src="https://github.com/user-attachments/assets/9e1dae41-aba9-45ab-9983-b1dd9f66b147">

          

5.6 Evaluation for Customer LLM Models
To run evaluations for own custom model,

•	From the dashboard, select the Upload Model option.
•	Follow the prompts to upload your LLM in a compatible format (e.g., TensorFlow, PyTorch).

Then follow rest of steps as above to create and view the evaluation report.

## 6.	Why Trust Matters in the Growing AI Space

As generative AI continues to grow, trust is becoming a top priority for enterprises. Missteps in AI deployment—whether due to privacy violations, unethical biases, or security vulnerabilities—can have grave consequences. Vijil addresses these concerns by providing a comprehensive framework to measure and improve the trustworthiness of AI systems. Their vision aligns with the needs of the industry: to make AI systems that are not only intelligent but also safe and reliable. With Vijil, you can ensure your LLMs are not only accurate but also aligned with ethical and societal standards. Start refining your models today!

## 7.	The Vision and the Future

Vijil’s long-term goal is to create a trusted operating system for the development and deployment of AI agents. The startup envisions a future where cognitive AI assistants work seamlessly with humans to automate tasks while maintaining the highest standards of security and ethical performance. By partnering with enterprise customers and academic researchers, Vijil is contributing to open-source projects and driving innovation in AI safety and trust.
![image](https://github.com/user-attachments/assets/ae335fd3-9950-49b7-a28b-9ec057e114ba)
