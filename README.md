# Library-Semantic-Search-Ontology
# Library Semantic Search Ontology (Protégé / OWL)

## Overview
This project presents a prototype ontology designed in **Protégé** using **OWL** to support an AI-enabled search experience for a community-funded local library. The goal was to improve service efficiency by enabling visitors to search for books more accurately using structured domain knowledge, rather than relying only on keyword matching.

## Problem Context
The library holds a wide range of books (fiction and non-fiction; adult and children’s collections). The Library Manager aims to introduce an AI-powered system that helps users:
- find relevant books quickly,
- discover similar titles,
- filter by meaningful attributes (e.g., genre, audience, author, format),
- and reduce staff time spent handling routine search queries.

## Proposed Solution
I designed a **domain ontology** to act as the “knowledge backbone” for a semantic search engine. The ontology models key entities and relationships in the library domain and supports reasoning and structured querying.

### Core Concepts Modelled
- **Book**
- **Author**
- **Genre / Category**
- **Audience** (e.g., Adult, Children, Young Adult)
- **Format** (e.g., Print, eBook, Audio)

### Key Relationships (Examples)
- `hasAuthor` (Book → Author)
- `hasGenre` (Book → Genre)
- `intendedForAudience` (Book → Audience)
- `hasFormat` (Book → Format)

These relationships enable semantic filtering and inference beyond simple keyword search.

## How Ontology Supports an AI-Powered Search Engine
The ontology can support a semantic search workflow such as:
1. User enters a query (e.g., “children’s mystery books”).
2. The system maps query terms to ontology concepts (Audience=Children, Genre=Mystery).
3. The search engine retrieves matching instances and can infer related results (e.g., sub-genres, equivalent categories).
4. Results can be ranked or expanded using ontology relationships (e.g., similar genres, same author, same audience).

## Tools & Technologies
- **Protégé** (ontology development)
- **OWL / Description Logic** (formal modelling)
- **Reasoner** (e.g., HermiT/Pellet — depending on setup) for consistency checking and inference

## Strengths of the Design
- **Structured knowledge representation**: formalises library information into reusable concepts and relationships.
- **Improved search precision**: supports meaning-based filtering (audience/genre/author) rather than keyword-only matching.
- **Extensible foundation**: the ontology can be expanded to include borrowing status, availability, user preferences, or recommendations.

## Limitations & Areas for Improvement
- **Prototype scope**: a production system would require integration with a catalogue database and a query layer (e.g., SPARQL endpoint).
- **Data population**: the ontology’s usefulness depends on consistent metadata and sufficient instances.
- **User query interpretation**: mapping natural language queries to ontology concepts would require an NLP component or controlled vocabulary.

## Repository Contents
- `/ontology/` — OWL ontology file(s)
- `/docs/` — report and supporting documentation
- `/screenshots/` — modelling evidence (class hierarchy, properties, reasoning)

## Author
**Oghenevurie Lauretta**
