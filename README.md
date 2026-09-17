# RepoReco-Team

RepoReco-Team is an organization formed by three Master's students in AI at Le Mans University.
Our goal is to design and compare several algorithms for **GitHub repository recommendation**, combining classical recommender-system techniques with NLP-based approaches, as part of our Big Data coursework.

---

## Members

| Role        | Name            | Email                               | University Identifier |
|-------------|-----------------|--------------------------------------|------------------------|
| Developer   | Maelig Pesantez | maelig.pesantez.Etu@univ-lemans.fr   | @e2103064               |
| Developer   | Luka Cognard    | Luka.Cognard.Etu@univ-lemans.fr      | @s2200371               |
| Developer   | Mewen Puren     | Mewen.Puren.Etu@univ-lemans.fr       | @s201509                |
| Supervisor  | Nicolas Dugué   | Nicolas.Dugue@univ-lemans.fr         | LIUM, Le Mans University |

---

## Organization Overview

RepoReco-Team focuses on building a **GitHub repository recommender system**, trained on a large corpus of repositories collected beforehand. The project explores several complementary recommendation strategies, from collaborative filtering to content-based and NLP-driven approaches, and compares their behavior — including on cold-start scenarios.

**Timeline:** M2 Big Data project, 2026

**Key repositories:**
- [Repo Recommender — main project](https://github.com/RepoReco-Team/repo-recommender)
- [Data Collection Pipeline](https://github.com/RepoReco-Team/data-collection)

---

### 1. Twin Repos Detection

Given a repository provided by the user (README, description, topics, etc.), this module finds existing repositories that are functionally or thematically equivalent — including the detection of **abandoned or discontinued "twins"**, to help users discover actively maintained alternatives to a stale project.

---

### 2. Astrological Stack

A lighter, "Buzzfeed-style" quiz-driven recommender: the user answers a short quiz (and/or we analyze their GitHub profile), and the algorithm recommends a repository based on the resulting "developer profile" — a playful entry point into the more serious recommendation engines below.

---

### 3. Classical Collaborative Filtering

Recommends a repository to a user based on the behavior of similar users (user-based / item-based collaborative filtering). This module is also used as a testbed for **cold-start scenarios**, where very few user interactions are available.

---

### 4. Content-Based Recommendation (RAG / Topic Modeling)

A content-based approach relying on each repository's README, description, and topics:

- A **RAG-style** retrieval pipeline built on top of README content
- An improved variant using **Topic Modeling with BERTopic** to better capture the semantic themes of a repository

---

### 5. Trending

A simple popularity-based baseline, recommending repositories based on trending signals (stars, activity, recent growth), used as a reference point to evaluate the other approaches against.

---

## Repository

**Main Repository:** [Repo Recommender](https://github.com/GitRepoReco/Analyse-github)
**.github:** [.github](https://github.com/GitRepoReco/.github)
