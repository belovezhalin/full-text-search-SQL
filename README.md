# Full Text Search in Microsoft SQL Server

This project demonstrates how to use **Full Text Search** in Microsoft SQL Server, utilizing the **Northwind** and **AdventureWorks2022** databases. Full Text Search is a powerful feature in SQL Server that allows you to search for complex patterns in textual data, such as keywords, phrases, or even partial word matches. This is particularly useful when working with large datasets or when you need to perform more advanced search queries than those supported by standard SQL `LIKE` clauses.

## Project Overview

The project includes several examples and use cases to help familiarize you with Full Text Search functionality in SQL Server. The **Northwind** and **AdventureWorks2022** databases, which are a sample databases widely used for learning purposes.

## Key Features of Full Text Search

- **Indexing**: Full Text Search uses specialized indexes called Full-Text Indexes to speed up text search operations. These indexes are created on one or more columns in a table that contain text data (e.g., `VARCHAR`, `TEXT`, or `CHAR` columns).
  
- **Search Capabilities**:
  - **Word Prefix Search**: Search for words with a specific prefix (e.g., searching for "advent" would return "adventure," "adventurous," etc.).
  - **Fuzzy Search**: Find words that are similar to a specified word.
  - **Phrase Search**: Search for exact phrases (e.g., searching for `"high performance"` would return results where these two words appear together in that order).
  - **Ranking**: Full Text Search can rank search results based on relevance, providing more accurate and relevant results.

## Use Cases: Basic Text Search

How to use simple queries with the `CONTAINS` or `FREETEXT` functions to search for individual words or phrases in columns with text data.

Example:
```sql
SELECT * 
FROM Products
WHERE CONTAINS(ProductName, 'bike');
```
