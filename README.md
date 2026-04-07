# Project Title - Building Chatbot for Technical Documentation using LangChain and RAG

# Goal - 
Create a context-aware chatbot which can explain dashboard warnings and recommend actions while driving by integrating a car manual with an LLM using LangChain and Retrieval Augmented Generation (RAG).

# Description -
A well-known car manufacturer is looking at implementing LLMs into vehicles to provide guidance to drivers. Integrate a car manual with an LLM to create a context-aware chatbot. This context-aware LLM can be hooked up to a text-to-speech software to read the model's response aloud. Integrate several pages from a car manual that contains car warning messages and their meanings and recommended actions. This particular manual, is stored as an HTML file.

# Libraries - 
1) from langchain_core.prompts import ChatPromptTemplate 
2) from langchain_openai import ChatOpenAI, OpenAIEmbeddings
3) from langchain_community.document_loaders import UnstructuredHTMLLoader
4) from langchain_core.runnables import RunnablePassthrough
5) from langchain_text_splitters import RecursiveCharacterTextSplitter
6) from langchain_chroma import Chroma

# Main Functions - 
llm = ChatOpenAI(model='gpt-4o-mini', temperature=0)
embeddings = OpenAIEmbeddings(model='text-embedding-3-small', openai_api_key=os.environ['OPENAI_API_KEY'])
