# LOW RANK ADAPTATION (LoRA)

Fine tuning methods, Rather than retrained the entire Model from the ground . 
Low rank metrices to the model

Google paper "Attention is all you need "
fined tuned weights added to base model 
Base Model remain unchanged
very effecient 
    * storage
    * trining 
    * interference
Adapter layer --- added to the top of the base model

# Another fine Tuning -- RAG

Open book exam 
instead of relaying on the LLM 
Search on the external articles 

Pros , 
* faster and cheap 
* semantic search for  vector stores.
* prevent hallucination -- where model is not trained for this information.
* AI Search 
* techincally you are not training the model

Cons
* overcomplicated search - multiple places, alot of token
* sensitive to prompt
* non-deterministic
* can still hallucinate
* very senstive to the relevancy of the information you retrieve

Choosing a database [Knowledge base data store] for RAG
* Graph database - Neo4J
* Opensearch - traditional text search TF/IDF
* vector db - COMMON
* Elasticsearch / opensearch can function as vector db - often in amazon bedrock

# embedding - giant vector

* similar are placed close together 
* stored in vector database

examples of vector DB
* opensearch / elastic search 
* sql 
* neptune
* redis 
* mongodb
* cassandra

Purpose driven vector DB
* Pinecone, weaviate (commercial)
* chroma , marqo, vespa,qdrant, lanceDB, Milvusm vectordb(opensource)
