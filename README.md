java c Comments from 02/09 meeting with Prof Rajesh
Total $2000 budget to use!
Could use a not so L model if locally
Project Template:
- Problem statement
- Various options [Pros and Cons]
- Specific Approaches and implementation [Split to 2 if need be]*
- What could be done/improved.
- Conclusion Future directions
Project Template: AI Teaching Chatbot ( based on the above requirements )
1) Problem Statement
In traditional education, students often struggle to receive individualised attention, especially in large classes or online environments. The increasing demand for personalised learning, cost-effective teaching, and 24/7 availability has spurred interest in AI-powered teaching chatbots. These AI chatbots aim to provide real-time, tailored assistance to students, filling gaps in human instruction and making education more accessible. However, challenges related to the effectiveness, adaptability, and human-like interaction of such chatbots remain to be addressed.
2) Various Options (Pros and Cons) a) Rule-Based AI Chatbots:
● Pros:
○ Easy to implement.
○ Clear, predictable responses.
○ Works well for structured or fact-based lessons. ● Cons:
○ Limited in scope and flexibility.
○ Unable to understand complex questions or adapt to unstructured dialogue.
○ Requires frequent manual updates.
b) Machine Learning-Based Chatbots:
● Pros:
○ Can learn from interactions, improving over time.
○ More flexible and capable of handling open-ended questions.
○ Can offer personalized responses based on user data.
● Cons:
  
 ○ Complex to develop and maintain.
○ Requires a large amount of training data.
○ May struggle with ambiguous or nuanced questions.
c) Hybrid Models (Rule-Based + ML):
● Pros:
○ Combines predictability with adaptability.
○ Can handle structured lessons while adapting to more complex interactions.
○ More robust and scalable.
● Cons:
○ More resource-intensive to develop.
○ Requires constant tuning and maintenance.
○ Integration challenges between rule-based logic and machine learning
components.
d) Fine-tuning an Existing LLM:
○ Pros: Tailored to specific educational content, incorporating domain-specific knowledge and terminology, potentially improving performance on educational queries.
○ Cons: Requires extensive high-quality, domain-specific training data; computationally expensive; may struggle with providing up-to-date information.
e) Basic Retrieval Augmented Generation (RAG):
○ Pros: Merges the strengths of pre-trained language models with external knowledge retrieval, enhancing factual accuracy and access to current information. It’s also more flexible and easier to update than fine-tuned models.
○ Cons: Requires careful curation of the knowledge base; may face challenges with complex reasoning tasks requiring integration of multiple information pieces.
f) Advanced RAG Techniques (e.g., RAG Graphs):
○ Pros: Superior handling of complex queries and multi-hop reasoning, improved context understanding, and more natural and coherent responses.
○ Cons: Increased implementation complexity, higher computational demands, and as an evolving research area, it presents potential challenges.
g) Long Context Model
○ Pros: Ergonomically easier to use
○ Cons: Slow and expensive
 
 3) Specific Approaches and Implementation
a) Natural Language Processing (NLP) Integration:
● NLP helps the chatbot understand and process human language. Implementing pre-trained models like GPT or BERT can enhance the chatbot’s ability to interpret and generate relevant responses.
● Implementation:
○ Leverage APIs from cloud platforms (e.g., Google Cloud AI, IBM Watson) to
integrate NLP capabilities.
○ Fine-tune models using education-specific datasets to improve context
recognition and relevance in responses.
b) Knowledge Graphs and Rule-Based Engines:
● Create a structured database of knowledge and predefined rules to guide the chatbot’s responses for fact-based queries.
● Implementation:
○ Develop a comprehensive knowledge base that aligns with the curriculum.
○ Implement decision trees and if-then logic for specific topics (e.g.,
mathematics, history).
c) Adaptive Learning Algorithms:
● Personalise learning paths based on the student's performance and engagement. Use AI to assess learning gaps and adjust difficulty levels dynamically.
● Implementation:
○ Employ reinforcement learning algorithms to dynamically adjust the difficulty
of questions.
○ Collect student interaction data to continuously improve and tailor the
chatbot’s learning suggestions.
4) What Could Be Done/Improved
● Incorporation of Emotion Detection:
○ Chatbots could be enhanced with sentiment analysis to better gauge student
frustration or confusion and respond accordingly, mimicking the empathy of
human teachers.
● Multimodal Learning Support:
○ Integrating visual and audio aids into chatbot responses can create a more interactive learning environment, especially for complex subjects that require diagrams or step-by-step guidance.
● Enhanced Context Awareness:
○ Improve the chatbot’s ability to remember past interactions, allowing for more
meaningful and context-aware follow-up questions or lessons. ● Support for Multilingual Learning:
 
 ○ Expanding chatbot capabilities to multiple languages could help bridge educational gaps globally and make learning more accessible in non-English speaking regions.
5) Conclusion and Future Directions
AI teaching chatbots hold the potential to revolutionise education by offering scalable, personalised, and on-demand learning. While existing solutions show promise, there is room for improvement in emotional intelligence, contextual understanding, and multimodal capabilities. Future developme代 写Program、SQL
代做程序编程语言nts could focus on refining AI models to become more human-like in their interaction and empathy, as well as incorporating new advancements in AI to better detect and address student needs. These improvements would not only enhance the effectiveness of teaching chatbots but also broaden their applicability across different educational domains, cultures, and languages.
The future of AI-powered education could see chatbots evolving into integral tools that complement, rather than replace, traditional teaching, making learning more accessible and personalised worldwide.
- Look for existing tools and similar implementations we can leverage on to start from, don't need to start from scratch
- $2000 budget total for subscriptions, etc.
- Work towards a more clearly distribute workload by the end of sem
- By end of semester,
1. Goals and timeline for project
2. Individual report -> Specific literature, tools, techniques explored (beyond the combined
report, more of an individual journey that led to the combined result) 3. Group dissertation-> More like the final report
Meet every 2 weeks (fri afternoons 2pm+) - next meeting 13 Sep (Fri)
Week 12-13 presentation individual and group Decide and split Who doing what
Focus on ideation
Reasoning
Options and possibilities that have been explored
Documentation and citation
Plan for following semester: Gan Chart
Individual portfolio talk more about specific design choices
 
 [Tools and sources explored] Group dissertation is project report
5 . attention is all you need
4. handwritten digit recognition with backprop network : yan Lecun 3. An image is worth 16x16 words : ViT
2. LoRA
1. RAG for knowledge intensive task
Learning to summarise from human feedback
Open-source Chatbot UI (https://github.com/mckaywrigley/chatbot-ui) Setting up Chatbot UI:
Using local browser storage which would limit the features we can have due to:
1. Security issues
2. Limited storage and multi-modal use cases.
Hence, we would need to run a database in the backend. The Chatbot UI uses Supabase, which is a database infrastructure built on Postgres.
To run Supabase locally, we will be using Docker for easy setup, consistency across different environments, and to avoid compatibility issues. (Handle database, file storage, server functions, etc.)
To run LLMs with Chatbot UI locally, we need to install Ollama. Packages everything needed to run an LLM locally – model weights, configurations, etc – into a single Modelfile.
Running Chatbot UI
The login screen is an authentication that is running locally in the Docker instance of Superbase.
    
 Using LLMs
1. Hosted (API Keys): Most of them require a subscription to be able to use the API Keys.
2. Local: Models can be downloaded locally using Ollama. Usability depends on RAM
availability.
Uploading file error:
   - Implementation issue?
Potential Uses or References:
The developers of Chatbot UI mentioned that "We support forks. This is all MIT licensed open-source code so feel free to fork it, tear it up, and do whatever you want with it. It is totally on you to build whatever you want, this is merely our take on it." and "We encourage you to fork the code and implement your own backend."
- Possibly take reference to the UI for our own chatbot - the way they structured it to be used with multiple different LLMs of the user’s choice.
- We can make use of Ollama for local deployment of LLMs, depending on our implementation.
- Similarly to Supabase, we can use BaaS for easier backend management - file storage and database management, authentication and user management, etc.
For BaaS, we can consider Supabase or Firebase (a similar tool that I have used before): Firebase:
- Database - Uses Firestore (NoSQL document-based database) known for real-time data synchronisation, making it ideal for chat applications, collaborative tools, and other use cases where real-time updates are crucial.
- Authentication - Firebase Authentication supports a wide range of methods including email/password, OAuth (Google, Facebook, Twitter), and phone authentication.
- Storage - Offers Firebase Cloud Storage, primarily designed for handling large amounts of unstructured data like images, videos, and other binary objects.
     
 Designed to store files like images, videos, audio, and other media. Optimised for storing and retrieving large files and can integrate well with Firebase Authentication and Firebase Database services for managing file access.
(Data stored in Firebase Cloud Storage can be accessed via URLs or file paths and has features like access control, automatic scaling, and data redundancy)
Supabase:
- Database - Built on PostgreSQL (relational SQL database) which is good for
applications where structured data, complex querying, and transactional integrity are
required.
- Authentication - Supabase Authentication is based on GoTrue and supports
email/password, OAuth providers (Google, GitHub, Twitter), and third-party providers.
Fully integrated with PostgreSQL for role-based access control.
- Storage - Provides Object Storage using S3-compatible storage, which is more
flexible and can also be used for handling large media files and other content. Also able to store and manage files such as images, videos, and documents, and access can be controlled through the Supabase Auth system.
(Files are stored as objects and can be accessed via URL or API)
   
 Meeting #2 (04/10)
More references with information
Authentic References scientific publications
Focus more on the ML part, Frontend and Backend can be bootstrapped, so all hands on deck for Machine Learning Part
By CA1, develop basic applications for tasks such as chatbot to query models etc.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
