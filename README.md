# **LinkedUp: AI-Powered Startup Matchmaking Tool**  

 

## **Overview** 

Finding the right co-founder or job opportunity can be time-consuming and frustrating. **LinkedUp** aims to use data to connect like-minded entrepreneurs and help them build successful startups. 

 

Using AI techniques, LinkedUp analyzes multiple attributes of an entrepreneur—including **language, position, education, recommendations, volunteer experience, courses, and relevance scores**—to determine the best possible matches. 

 

## **How It Works** 

### **1. Data Collection & Processing** 

- Extracted **active users** from LinkedIn profiles (users with at least one post and education entry). 

- Scraped LinkedIn post content and classified them into **meta-topics** using NLP models. 

- Collected company-related news and success metrics from **Google News** to infer startup viability. 

 

### **2. AI-Powered Matching** 

We implemented three key components to compute the **match score** between users: 

- **Foreseeing-Success NN:** A neural network trained on **co-founder data + Google News** to predict startup success. 

- **Post Labeling:** Classifies user discussions into **meta-topics** for interest-based compatibility. 

- **Education Compatibility:** Uses **Sentence Transformers + Cosine Similarity** to find complementary educational backgrounds. 

 

### **3. Scoring Function** 

Our **match score** is a weighted sum of the following: 

Score(u₁, u₂) = w₁ ⋅ successNN(u₁, u₂)  + w₂ ⋅ sim(u₁₍interest₎, u₂₍interest₎) + w₃ ⋅ comp(u₁₍education₎, u₂₍education₎)


The **weights (w1, w2, w3)** were learned using **Logistic Regression** on real co-founder data.


To run our notebook you will have to download the notebook and using the data located in dbfs you will be capable of running all our cells and find the next co-founder! 


 
