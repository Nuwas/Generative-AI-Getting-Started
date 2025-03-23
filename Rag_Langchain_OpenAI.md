


RAG + Langchain Python Project: Easy AI/Chat For Your Docs

* Prepare the data.
* Query for relevant data.
* Craft the response

  Load .md (Mark Down) data, so thats the <b>Document</b>.
  Split the Document to <b>Chunks</b>.
  To query this chunks, we need to turn this into a <b>chromaDb</b> database.
  So at this point the <b>vector-db</b> is created, ready to start using it.

  Source/Load/Tranform/Embed/Store/Retrieve

  <b>Embeddings</b> are vector representation of text that capture their meaning.
  This is list of <b>numbers</b>. Its sort of <b>coordinates in multi-dimensional space.
  If two pieces of text are closely related to each other, that means, then those coordinates will also be close together.

  Then distance between these vectors can be calculated easily using cosine similarity or euclidean distance.
  We have functions to do that, its going to give us a single number, its going to tell us how far these two vectors are apart. 

  Use langchain <b>evaluator</b> utility to find the embedding distance between the two vectors.
  Now we can use the openAPIEmbedding function to fetch the data from ChromaDB.
  So we can pass the query and mention the number of results we want to retrive.
  So result is going to be a list of tuple.
  Each tuple is a document and its relevant score.

  Now we have found the relevant chunks for our query, we can feed this to openAI to create a high quality response.
  So create a <b>prompt</b> template to create a prompt.
  Pass the placeholder <b>{context}</b> and <b>{query}</b> to the template and 
  Now send that prompt to the <b>llm model</b> of our choice, in our exmaple we are using chatOpenAPI, then we will have our response.
  
