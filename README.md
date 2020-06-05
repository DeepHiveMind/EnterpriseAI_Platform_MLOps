# Production machine learning system| Real World ML System | Enterprise AI Platform MLOps 
This repository intends to offers 
- A Real-world vision and recepie of the `design, development and operation` of **production machine learning systems & operation**.
- A curated list of tools, frameworks and open source libraries that helps AI/ML Engineers `Deploy, monitor, version, scale, and secure` production machine learning. 
- State of Machine Learning Operations in Y'2019.

<img src="images/Recent_Poll_PipelineAI_July2019_1.JPG" width="900" height="400" border="10">  

- A prescriptive view of constituents, constructs and tools of a **comprehensive, operational & production Machine learning ecosystem** that any good **"Enterprise AI Platform"** must intend to stich/chain together under its hood. Genrally "Enterprise AI Platform", such as H20.ai/Alteryx/HopsML/PipelineAI etc are powered by **Custom MLOPS** with the objective to *attempt to offer* essential high level MLOps constructs.
- A Deep Dive View into:
    - ML Model Reproducitbility and Versioning
    - Production Machine Learning Orchestration
    - Explainablility of Black Box Models (a pillar of AI Trust)
    - **Ethical AI (a pillar of AI Trust)** with adequate deatiling around "Ethical AI Frameworks", "Codes of Ethics", "Guidelines", "Regulations" et al. [Ethical AI](/README_Ethical_AI.md).


**A Quick Rundown:**

- [INSPIRATION for MLOPS](#INSPIRATION_for_MLOPS)
- [High level constructs of MLOPS](#High-level-constructs-of-MLOPS)
- [Detail References to the Constructs and Tools of MLOPS](#Detail-References-to-the-Constructs-and-Tools-of-MLOPS)
- [Product Machine Learning System Y2019 A Video](#Product-Machine-Learning-System-Y2019-A-Video)

## INSPIRATION for MLOPS

**WHY DO WE NEED MLOPS?**

1. SIMPLY PUT ACROSS:

**SMALL DATA SCIENCE PROJECTS**/POC/MVP has lesser complexities, than **ENTERPRISE DATA SCIENCE SYSTEM**.

- A simple **workflow of 'Build/Prepare' --> 'Train' --> 'Evaluate'--> 'Deploy' --> 'UI' (a simple WebApp)** does relatively very well with **SMALL DATA SCIENCE PROJECTS**/POC/MVP.
- But, as the Data Science(DS) requirements, productionization and, hence DS Teams grows, whole lot of new issues starts popping up in **ENTERPRISE DATA SCIENCE SYSTEM**. Such as 
    - 'Increased complexities in flow of Data, 
    - Data Science Tools proliferation (each siloed deptt would start using their own preferred DS tools, Serving Models become increasingly harder, 
    - when stuff goes wrong it's hard to trace back, 
    - Infrastructure needs, its governance starts growing rapidly
    - & many More (See, whole lot of issues which is now being faced with Enterprise large Data Lakes)
    
THEREFORE, the SIMPLE WORKFLOW which worked pretty well for 'SMALL DATA SCIENCE PROJECTS' starts failing and crumbling under the complexities of 'ENTERPRISE DATA SCIENCE SYSTEM'.

|**SMALL DATA SCIENCE PROJECTS**| **ENTERPRISE DATA SCIENCE SYSTEM**|
| :---: | :---:|
| Workflow | Workflow| 
|<img src="images/Small_DataScience_Project.JPG" width="500" height="200" border="10">|<img src="images/mlops1.png" width="500" height="200" border="10">|
| Workflow Job well done | Still lot missing in the Workflow :smiley:| 



2. WHEN THE RUBBER HITS THE ROAD:

As and when, the SMALL DATA SCIENCE PROJECTS/POC/MVPPOC/MVP hits the REAL WORLD SYSTEM, it starts to face new set of Challenges, 
such as 
- **Need to Re-Train**: After Pushing Your Model to Production, Your Model is already Out of Date. Google updates its SEO model/algorithm  on average 500 times per year. [Ref](https://www.seoblog.com/google-penguin-panda-refresh/#:~:text=Of%20course%2C%20these%20are%20not,average%20500%20times%20per%20year.)
- **Slow**: Need to Quantize and Speed Up Predictions
- **Biased**: Needs to Validate Trained ML Binary/ Service/ servable in any form for Bias detection Before Pushing 
– **AI/ML Service Routing (If Broken)**: Need to A/B Test/ Multi Armed Bandit in Production 
– **Security Vulnerability (If Hacked)**: Need to Train With Data Privacy (All your Data & other security is for a toss now as the Makert exposed AI Model has the essence of the underlying data.
       

3. HIDDEN TECH DEBT IN REAL WORLD ML SYSTEM:

<p align="center"> # HIDDEN TECH DEBT IN ML SYSTEM- NIPS/GOOGLE 2015</p> 

<p align="center"> # Only a SMALL FRACTION of REAL-WORLD ML SYSTEMs is composed of the ML CODE</p> 

_Courtsey Google NIPS 2015

<p align="center">
<img alt="Google NIPS 2015" src="https://image.slidesharecdn.com/4brookewenigjulesdamji-180612221342/95/a-tale-of-three-deep-learning-frameworks-tensorflow-keras-and-deep-learning-pipelines-with-brooke-wenig-and-jules-damji-5-638.jpg?cb=1528841699">
</p>

<p align="center">[HIDDEN TECH DEBT IN ML SYSTEM- NIPS/GOOGLE 2015](https://papers.nips.cc/paper/5656-hidden-technical-debt-in-machine-learning-systems.pdf)</p>  


<p align="center"> # Hardest part of AI isn't AI, but it's Data & productionization</p> 

<p align="center"> # Productionization/Industralization Machine Learning Systems</p> 
    
MLOPS IS THE SILVER BULLET

## High level constructs of MLOPS

Any **"Enterprise Data Science System" / "Enterprise AI Platform"** must intend to stich/chain together at least the essential & high level constructs of MLOPS under its hood. Genrally "Enterprise AI Platform", such as H20.ai/Alteryx/HopsML/PipelineAI etc are powered by **Custom MLOPS** with the objective to *attempt to offer* following key high level AI/ML constructs:
   
    - **"AI/ML Dataset Annotation"** 
    ```
     --o 'Image Annotation framework' (VoTT, LabelImg, VIA ) 
     --o 'NLP/ Text Annotation framework' (spacy, explosion.ai,)
     --o 'Audio & Speech Annotation framework' (Web-Based Audio Sequencer, CrowdCurio/audio-annotator, annotationpro)
     --o 'Ontology/Knowledge Graph Annotation framework' (Apache Jena)
    ```
    
    - **"AI/ML Pipeline"** 
    ```
     --o  AI/ML Model 'Build/Prepare' (Notebook/ Visual AI Studio with dockerized support to AI/ML Libraries-TF/PyTorch/SparkML/XGboost/,  EDA libraries, Pre-processing libraries, Data Augmentation Libraries, Adversarial Robustness Libraries) 
     --> 'Train' (Computation load distribution frameworks for 'Distributed/Standalone tarining' on accelerated neural network hardware -GPU/TPU/CPU- with support for real time Training Visualization - TensorBoard/VisualDL)
     --> 'Evaluate'
     --> 'Deploy' (AI-as-a-Service -RESTful/gRPC API- , or, Binary Servables, or, Edge/Mobile deployment)
     --> 'Model Serialization & Quantization'  
     --> 'Monitor' (Data drift & Concept drift with Alert) 
     -->  'Automated Re-training pathway' (Airflow)
    ```
    
    - **"Automated ML"** 
    ```
      'HPO' - Hyper Parameter Optimization,
      'Randmoized/Grid Serach',
      'NAS' - Neural Architecture Search,  
      'AutoML'         
    ```
       
    - **"Comprehensive AI Governances"** 
    ```
     --o 'AI TRUST' - Explainable AI, Ethical AI, Fair AI, Feature Management & Stoarge, 'Model and Data Versioning',
     
     --o 'AI Collaboration, Sharing & Exchange' - AI/ML APIs Authenticated Sharing, Fature Set Authenticated Sharing, Model Binaries Authenticated Sharing, Notebook /Model Code Authenticated Sharing,
     
     --o 'AI Security' - Privacy Preserving Machine Learning, AI/ML API Security (Authentican & Authorization)
     
     --o 'AI Scalability' - Autoamted Load Balancing, Service Routing, AutoScaling
     
    ```
    - **"AI Operation Cost Optimization "** 
     ```
      --o 'CI framework' (Jeknis/ Travis CI)
      --o 'CD framework: Containerized & Container orachasteration by Container-as-a-Service ' (Docker, Kubernetes, Mesos)
      --o 'Microservice governance framework for Plug/Play of AI/ML system' (API Gateway, Microservice Service Mesh, Microservice Service Registry, Microservice Service Discovery, Microservice service internal communication protocol 
      --o 'Serverless Framework' (FaaS - OpenWhish/ OpenFaas, KNative)
      --o 'Application Load Balancer, Autoscaling, MultiZone Replication'
     ```       

     - "Comprehensive **DataOps"** 

        


## Detail References to the Constructs and Tools of MLOPS

| | | | |
|-|-|-|-|
| [🧵 Data pipelines & ETL]()| [💸 Data Stream Processing]() |[🗞️ Data storage]() |[🏷️ Data Labelling]()|
| [🌀 Feature engineering]()| [🎁 Feature Stores]()| [📓 Reproducible Notebooks]()|[🏁 Model Orchestration]()|
| [🗺️ ML Training Computation distribution]() | [📊 ML Training & Indutrial Visualisation frameworks]() |[⚔ Adversarial Robustness]() |[📥 Model serialisation]() |
|[🔍 Explaining predictions & models]() |[🔏 Privacy preserving ML]() | [📜 Model & data versioning]()|| [🧮 Optimized calculation frameworks]() |
|[🤖 Neural Architecture Search]()| [📡 Functions as a service]() | [🔠 Industry-strength NLP]() | [💰 Commercial Platforms]() | 



## Product Machine Learning System Y2019 A Video

<table>
  <tr>
    <td width="30%">
        This <a href="https://www.youtube.com/watch?v=Ynb6X0KZKxY">10 minute video</a> provides an overview of the motivations for machine learning operations as well as a high level overview on some of the tools in this repo.
    </td>
    <td width="70%">
        <a href="https://www.youtube.com/watch?v=Ynb6X0KZKxY"><img src="images/video.png"></a>
    </td>
  </tr>
</table>

