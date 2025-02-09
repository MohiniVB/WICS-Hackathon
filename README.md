# WICS-Hackathon

## Medical AI Chatbot
## PLEASE NOTE: I COULD NOT COMPILE A DATABASE FOR THE SECOND SOLUTION WITH MY CURRENT RESOURCES. THE SOLUTION IS CURRENTLY HYPOTHETICAL.

### Overview
This repository contains two versions of a medical AI chatbot designed to assist in gathering patient medical history. The chatbot utilizes OpenAI for natural language processing and is progressively enhanced to improve the depth and accuracy of the medical history it collects. Below, we explain the differences between the two versions of the chatbot.

### Version 1: Basic Medical Chatbot (OpenAI + Predefined Questions)
#### Description:
The first version of the medical chatbot uses OpenAI's language model along with a predefined list of medical history questions. It is designed to collect a patient's medical history in a structured manner, following the typical flow of medical history-taking:

1. Demographics (age, gender, etc.)
2. Main complaint (reason for the visit)
3. History of present illness
4. Past medical and family history

#### Features:
- Predefined Question List: The chatbot is equipped with a list of standard questions to ask the patient.
- Follow-Up Questions: If the patient’s response indicates a need for further questioning, the AI generates follow-up questions to dive deeper into the issue.
- No Database Reference: The chatbot operates solely based on the predefined list of questions and does not reference any external databases or previous patient histories.
#### Limitations:
- No Personalization: The chatbot is limited to the set questions and does not personalize its questioning based on previous conversations or cases.
- Simple Logic: It relies primarily on OpenAI's natural language capabilities to interpret responses and ask follow-up questions but does not analyze patterns in previous patient interactions.

### Version 2: Advanced Medical Chatbot (OpenAI + Pinecone + Medical History Database)
#### Description:
The second version of the medical chatbot is significantly more advanced, utilizing OpenAI, Pinecone, and a database of previous patient-doctor medical history conversations. This version aims to enhance the chatbot's ability to ask relevant questions based on real-world cases, thus improving the quality of the medical history collected.

#### Features:
- OpenAI + Pinecone: Uses OpenAI for natural language processing and Pinecone for vector-based search, which allows the chatbot to retrieve similar cases from a database of previous medical conversations.
- Medical History Database: A database of patient and doctor medical conversations is used to cross-reference and identify relevant cases. The chatbot analyzes these historical interactions to determine whether additional questions should be asked.
- Contextual Understanding: The chatbot has access to prior patient-doctor conversations and uses this context to inform its questioning, ensuring a more tailored and accurate history-taking process.
- Dynamic Question Generation: Based on the similarity of the current case with previous ones, the chatbot can identify knowledge gaps and ask more specific or relevant questions to gather a thorough medical history.

#### Advantages:
- Personalized Interactions: By referencing prior conversations, the chatbot can personalize its responses and adapt to specific patient needs.
- Contextual Awareness: The use of a large database of past medical histories allows the chatbot to better understand the nuances of medical conversations and provide more targeted follow-up questions.
- Improved Accuracy: The database allows the chatbot to identify patterns in responses and adjust its questioning based on previous similar cases.

#### Limitations:
- Database Dependency: The performance of the chatbot heavily depends on the quality and scope of the medical history database it has access to.
- Complexity: With the integration of Pinecone and the database, the second version requires more resources and setup compared to the first version.
