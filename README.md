# Coffee Shop AI Chatbot 🚀☕️

Welcome to the Coffee Shop AI Chatbot project! This repository includes all the resources, code, and instructions to help you develop an intelligent chatbot aimed at enhancing customer service within a coffee shop app. By harnessing the capabilities of LLMs (Large Language Models), Natural Language Processing (NLP), and RunPod's infrastructure, this chatbot efficiently manages order-taking, answers complex menu inquiries, and provides personalized product suggestions—all integrated into a React Native mobile application.

# 🎯 Project Summary
This project aims to build a highly intelligent **agent-driven chatbot** capable of:
* Handling live customer interactions, including order placements.
* Addressing menu-related questions, such as ingredients and allergens, using a **Retrieval Augmented Generation (RAG) system**.
* Offering tailored product recommendations via a **market basket analysis engine**.
* Streamlining the ordering process by capturing accurate and structured details.
* Filtering out irrelevant or inappropriate questions using a Guard Agent for safe, high-quality conversations.

## 🔧 Key Learning Outcomes
Through this project, you will get practical experience in:
* Deploying your own LLM using RunPod.
* Creating an agent-based system with specialized agents, such as Order Processing, Details, and Guard agents.
* Configuring a vector database to store coffee shop menu and product details.
* Utilizing Retrieval-Augmented Generation (RAG) to deliver precise, detailed responses.
* Training and deploying a recommendation system.
* Building a React Native app that integrates this robust chatbot.

## 🧠 Agent-Based Chatbot Design
![Chatbot Agent Architecture](./images/chatbot_agent_architecture.jpg)

The chatbot utilizes a modular, agent-based architecture, where every agent handles a specific task, ensuring smooth and effective user interactions. This modularity allows the chatbot to carry out complex actions by distributing them among specialized agents, making the system highly adaptable and scalable.

### 🤖 Core Agents in the System:
1. **Guard Agent:**
   This agent functions as a gatekeeper, monitoring incoming queries to ensure only relevant and safe messages proceed to other agents. It blocks inappropriate or irrelevant content, ensuring smooth user engagement.
   
2. **Order Taking Agent:**
   Responsible for guiding customers through the order process, this agent utilizes chain-of-thought prompting to mimic human-like decision-making. It ensures that all order details are captured in a clear and structured manner, improving order accuracy.

3. **Details Agent (RAG System):**
   Powered by a Retrieval-Augmented Generation system, this agent addresses detailed customer questions regarding the coffee shop’s menu, such as ingredients, allergens, and other FAQs. It retrieves relevant data from the vector database and uses language generation to provide accurate answers.

4. **Recommendation Agent:**
   This agent offers personalized product suggestions by working with a market basket analysis engine. When triggered by the Order Taking Agent, it analyzes the customer’s current order or preferences and suggests complementary items, enhancing upselling opportunities or helping users discover new products.

5. **Classification Agent:**
   The decision-making agent in the system, this agent classifies user queries and directs them to the appropriate agent based on intent, whether it's for recommendations, orders, or detailed menu information.

### ⚙️ Agent Collaboration
The agents work in sequence to process user inputs:

1. Customer queries are initially reviewed by the Guard Agent.
2. If valid, the Classification Agent determines the user’s intent (placing an order, asking for details, or seeking recommendations).
3. The query is routed to the respective agent:
   * The Order Taking Agent handles order-related requests.
   * The Details Agent retrieves menu information.
   * The Recommendation Agent suggests complementary products.

## 📱 React Native Coffee Shop App
![Coffee Shop App Interface](./images/mobile_app.png)

This React Native app serves as the user-facing interface, allowing customers to interact with the AI-powered chatbot, explore the menu, and place orders. Designed for user convenience, the app integrates real-time customer service through the chatbot, enabling users to receive personalized product recommendations, place orders, and learn more about menu items.

### Key App Features:
* **Landing Page:** Welcomes users to the coffee shop experience.
* **Home Page:** Displays featured products and menu categories.
* **Item Details Page:** Provides comprehensive product details, including ingredients and allergens.
* **Cart Page:** Allows customers to review and modify their order before checkout.
* **Chatbot Interface:** Facilitates direct interaction with the AI chatbot for assistance, recommendations, and queries.

# 📂 Project Structure
```bash
├── coffee_shop_customer_service_chatbot
│   ├── coffee_shop_app_folder # Contains React Native app code   
│   ├── python_code
│       ├── API/               # API for chatbot system
│       ├── dataset/           # Dataset for recommendation engine    
│       ├── products/          # Product data (names, prices, descriptions, images)   
│       ├── build_vector_database.ipynb             # Builds vector database for RAG   
│       ├── firebase_uploader.ipynb                 # Uploads products to Firebase    
│       ├── recommendation_engine_training.ipynb    # Trains recommendation engine 
```

## 🚀 Setup Instructions
Each folder contains specific setup instructions, allowing you to deploy the frontend, backend, and other components separately. 

## 🔗 Reference Links
* [RunPod](https://rebrand.ly/Runpod-Abdullah): RunPod Official Site - Infrastructure for deploying and scaling machine learning models.
* [Kaggle Dataset](https://www.kaggle.com/datasets/ylchang/): Source of the dataset for training the recommendation engine.
* [Figma app design](https://www.figma.com/design/PKEMJtsntUgQcN5xAIelkx/Coffee-Shop-Mobile-App-Design-(Community)?node-id=421-1221&node-type=FRAME&t=bakGV2g59KQ7cPBi-0): Design mockups for the app’s user interface.
* [Hugging Face](https://huggingface.co/meta-llama/Llama-3.1-8B-Instruct): Repository for Llama LLMs used in this chatbot.
* [Pinecone](https://docs.pinecone.io/guides/get-started/quickstart): Pinecone Documentation - Guide for using the vector database.
* [Firebase](https://firebase.google.com/docs): Firebase Documentation - Managing app data for the coffee shop app.
