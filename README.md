# Netflix Content Recommendation System

A content-based recommendation engine that suggests similar Netflix titles
based on genre, director, country, and content rating — built as Task 1
of the Auspify Technologies Machine Learning Internship.

## How it works

1. **Feature preparation** — combines genre tags (`listed_in`), director,
   country, and content rating into a single text feature per title,
   with genres weighted more heavily since they carry the strongest signal.
2. **Vectorization** — converts the combined text into numerical form using
   TF-IDF (`scikit-learn`).
3. **Similarity scoring** — computes pairwise cosine similarity across all
   8,700+ titles in the dataset.
4. **Recommendation** — given any title, returns the top-N most similar
   titles by similarity score.
5. **Evaluation** — a genre-overlap quality metric checks what fraction of
   recommended titles share at least one genre with the source title.

## Example

Returns 5 similar titles ranked by similarity score, along with type,
genre, and release year.

## Tech stack

- Python
- pandas
- scikit-learn (TfidfVectorizer, cosine_similarity)
- Google Colab

## Dataset

Netflix titles dataset (`netflix_titles.csv`) — 8,790 titles with columns:
`type`, `title`, `director`, `country`, `date_added`, `release_year`,
`rating`, `duration`, `listed_in`.

## Author

Abiram Prem
