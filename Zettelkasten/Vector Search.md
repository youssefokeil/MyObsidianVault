Created on: 05-07-2025 18:39, note by Youssef Okeil
Status: #idea #essay
Tags: #data_base #BaRead #AI

## Why similarities in data?
- this is very important in search, as it helps us find things that are similar in meaning not just in words. 
- instead of matching exact words. 
> Ex; let's say you're searching for a "book", you want the search engine to return also "stories", "novels", "comics". This is exactly how Vector search engines work. 

Below is a demonstration of https://projector.tensorflow.org/, that uses word2vec to vectorize words. You can see that by searching for "book", we got a lot of relevant words that have similar semantic meaning.

![[Pasted image 20250705185912.png]]
## Traditional Search vs Vector Search

| Traditional                                                                                                                    | Vector                                                                                                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| matching exact keywords. looks for the same words or phrases in documents and ranks them based on how often those words appear | understands the meaning behind words. Turns the query and data into numerical representations called vectors. Finds the results that are similar in meaning, even if exact words don't match |
| fast and simple                                                                                                                | smarter and more accurate                                                                                                                                                                    |
|                                                                                                                                | finds relevant results in complex and large datasets                                                                                                                                         |
### Steps for vector search
1. Data vectorization
	 - convert all data items in db into numerical vectors called embeddings
	 - the embeddings are generated ML models designed to capture the semantic meaning. Models like `word2vec`
2. Query vectorization;
	- when a user wants to search, the text is converted into a vector using the same embedding model or a compatible one
3. Similarity calculation
	- using mathematical similarity scoring such as [[Cosine Similarity]], [[Euclidean Distance]], [[Dot product similarity]]
4. Rank results and return them
	- ranking prioritizes intent and meaning over exact word matches
-----------------
# References
https://www.geeksforgeeks.org/nlp/what-is-vector-search/
