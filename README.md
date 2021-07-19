# Text Mining - TBBT Episode Plot Descriptions
To analyze The Big Bang Theory episode plot descriptions, I cleaned and preprocessed text data, and conducted basic text mining in R using data.world datasets - [Big Bang Theory Information](https://data.world/priyankad0993/big-band-theory-information).
## Introduction
Text mining is the process of transforming unstructured text data into a structured format and deriving high-quality information from unstructured data. The Big Bang Theory (TBBT) is an American television sitcom premiered on CBS in 2007 and concluded in 2019, with a total of 279 episodes over 12 seasons. In the “Big Bang Theory_IMDB” dataset, there are information about TBBT from IMDB and 281 observations of 8 variables. To conduct text mining on plot descriptions, the last column "Plot" was used.
## Text Data Cleaning and Preprocessing
   - Delete rows
     - To focus on the 279 episode, I deleted two episodes, one unaired pilot and one recap.
   - Clean Data
     - Convert letters to lower case
     - Remove white space
     - Remove punctuation
     - Remove stop words
   - Build a Corpus
   - Customize Stemmer and Stem Completion
     - First, I found that tm_map function in tm package and stemDocument function in SnowBallC package will change a letter 'y' at the end of a word to letter 'i', making word can not be completed perfectly. Thus, to perfrom stemming, I used hunspell_stem function instead. 
     - Then, I found that hunspell_stem function can sometimes return none or more than one results. Thus, to solve this problem, I created a function to either keep original term or return the last stem word.
     - Lastly, I found that stemCompletion function sometimes is not able to complete words using a dictionary. Thus, to ensure that it will keep stem word instead of returning NA in such case, I wrote for loop and if function.




viewed correlation of frequent terms, examined the association of a given word with other words, conducted 2-gram analysis, performed Hierarchical clustering, and analyzed episode plot descriptions by season. 

