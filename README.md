# Movie-recommender-system
A content-based movie recommender built on the TMDB 5000 dataset. Pick a movie, get 5 similar ones.
How it works
Each movie gets a "tag" — a combined blob of its genres, keywords, top 3 cast members, and director. Those tags get vectorized using CountVectorizer (5000 features, Porter Stemming to normalize words like "loving" → "love"), and cosine similarity scores tell us how close any two movies are.
One thing worth noting: actor names like "Sam Worthington" get their spaces removed before vectorizing — otherwise "Sam" matches across unrelated people and the recommendations go sideways.
Tech Stack
Python, Pandas, Scikit-learn, NLTK, Streamlit, Cosine Similarity
Dataset
TMDB 5000 Movies Dataset — 5000 movies with metadata on genres, cast, crew, and keywords.