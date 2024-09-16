# RAG-Hackathon

I made a simple app **"Chat with your pdf!"** that can interact with a bulky pdf and collect and dislay a precise answer using all the relevant points throughout the pdf.
It is built using the python language and run by streamlit

I made use of the following azure functionalities:
☀️ Azure AI Search
☀️ Azure Open AI
☀️ Azure Blob storage

Here, I have uploaded the pdf from my local device, for a more general use case I can make use of
☀ Azure Form Recognizer Service


The following is the architecture diagram! 
![Screenshot (14)](https://github.com/user-attachments/assets/514b2963-e62f-45b5-b8b5-7c73621931fc)

+ Step 1: The user asks a question or a query in the app user interface
+ Step 2: The server sends this query to azure AI Search
+ Step 3: The AI Search collects top meaningful results from blob storage which has split and indexed the pdf
+ Step 4: AI Search sends these results along with the query to Azure Open AI
+ Step 5: Azure Open AI uses this knowledge from the pdf to give a well tailored specific answer to the question rather than a vague one
+ Step 6: The app server get this answers and displays it to the user interface
