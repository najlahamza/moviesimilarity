# moviesimilarity
###  Table of contents  <br>
1- Introduction<br>
2- Import data<br>
3- tokenization and stemming<br>
4- TfidfVectorizer<br>
5- Create clusters<br>
6- calculate similarity distance<br>
7- dendogramme<br>
8- example<br>
9- conclusion<br>

#  1. Introduction
<br>
<p style="padding-left:120px">the purpose of this project is to find the degree of similarity between movies based on their Descriptions available on IMDb and Wikipedia.
</p>

# 2. Import data

<br>
<p style="padding-left:120px">we import data from csv file into a dataframe
</p>

### combine wiki and imdb plots 
<br>

<p style="padding-left:120px">The text in the two columns is similar, but they are written in different tones and linguistic expression<br>
so we wil combine both columns
</p>

# 3. Tokenization and stemming

### Tokenization
<br>
<p style="padding-left:120px">Tokenization is the process  by which we break down articles into individual sentences or words
<br>
    we will also remove tokens which are numeric values or punctuation
</p>

### stemming
<br>
<p style="padding-left:120px">Stemming is the process by which we bring down a word from its different forms to the root word
<br>
    For example, the words 'fishing', 'fished', and 'fisher' all get stemmed to the word 'fish'.
</p>

# 4. TfidfVectorizer

### Create TfidfVectorizer

<br>
<p style="padding-left:120px">TF-IDF recognizes words which are unique and important
<br>
    <br> TF (Term Frequency): how often a term appears
    <br> TDF (Inverse Document Frequency) : reduces the importance of a word if it frequently appears.
</p>

### Fit transform TfidfVectorizer
<br>
<p style="padding-left:120px;padding-right:120px;">Once we create a TF-IDF Vectorizer, we must fit the text to it and then transform the text to produce the corresponding numeric form of the data
</p>

# 5. Create clusters
<p style="padding-left:120px;padding-right:120px;">
    To determine how closely one movie is related to the other , we can use clustering techniques.
    <br> Clustering is the method of grouping together a number of items that presents similar properties
     <br>we will cluster our dataset by the genre of the movies
</p>
    
# 6. Calculate similarity distance
<div style="padding-left:120px;padding-right:120px;">
    Similarity distance is = <p style="font-weight:bold"> 1 - cosine similarity angle </p>
    <br> if the movies' plots are similar, the cosine of their angle would be 1 and then the distance between them would be 1 - 1 = 0.
     <br>the more the movies are similar , the more the distance is closer to 0
</div>

# 7. Dendograms
<br>
<div style="padding-left:120px;padding-right:120px;">
    We will plot a dendrogram of the movies whose similarity measure will be given by the similarity distance
</div>

# 8. Conclusion 
<div style="padding-left:120px;padding-right:120px;">
    <br>we have quantified the similarity of movies based on their plot summaries available on IMDb and Wikipedia, 
    <br>we separated them into clusters.
   <br> We created a dendrogram to represent how closely the movies are related to each other.
</div>
