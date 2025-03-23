


RAG + Langchain Python Project: Easy AI/Chat For Your Docs

* Prepare the data.
* Query for relevant data.
* Craft the response

  Load .md (Mark Down) data, so thats the Document.
  Split the Document to chunks.
  To query this chunks, we need to turn this into a chromaDb database.
  So at this point the vector-db is created, ready to start using it.

  Source/Load/Tranform/Embed/Store/Retrieve

  Embeddings are vector representation of text that capture their meaning.
  This is list of numbers. Its sort of coordinates in multi-dimensional space.
  If two pieces of text are closely related to eah other, that means, then those coordinates will also be close together.

  Then distance between these vectors can be calculated easily calculated using cosine similarity or euclidean distance.
  We have functions to do that, its going to give us a single number, its going to tell us how far these two vectors are apart. 

  
