# 📚 Library Semantic Search Ontology  
### Protégé · OWL · HermiT Reasoner · Knowledge Representation

---

## Overview

This project presents a prototype ontology developed in **Protégé** using **OWL** to serve as the semantic backbone of an AI-powered search engine for a community-funded local library.

The objective was to improve service efficiency by enabling structured, meaning-based search across books, copies, branches, accessibility features, and borrowing status — moving beyond simple keyword matching toward semantic reasoning.

---

## Problem Context

The library maintains a diverse catalogue including:

- Fiction and non-fiction titles  
- Adult and children’s collections  
- Multiple physical and digital copies  
- Branch-specific inventory  
- Borrowing and availability tracking  
- Accessibility features (e.g., Braille, Large Print, audio support)

The Library Manager aims to implement an AI-driven search system that allows users to:

- Find relevant books quickly  
- Filter by audience, genre, and accessibility needs  
- Check real-time availability  
- Identify branch location  
- Reduce manual staff queries  

---

## Ontology Design Approach

The ontology models both **bibliographic structure** and **operational library logic**, ensuring that abstract works, physical copies, and circulation states are represented distinctly and consistently.

### Core Classes

- `LibraryItem`
- `Book`
  - `FictionBook`
  - `NonFictionBook`
- `Copy`
- `Author`
- `Genre`
- `Audience`
- `LibraryBranch`
- `AvailabilityStatus`
  - `Available`
  - `OnLoan`
  - `Reserved`
  - `InProcessing`
  - `DueSoon`
- `AccessibilityFeature`
  - `LargePrint`
  - `Braille`
  - `AudioAccessible`
  - `DyslexiaFriendlyFont`
  - `EBookScreenReaderCompatible`

---

## Key Object Properties

- `hasCopy` (Book → Copy)  
- `hasAuthor` (Book → Author)  
- `hasGenre` (Book → Genre)  
- `hasAudience` (Book → Audience)  
- `hasFormat` (Copy → Format)  
- `locatedAt` (Copy → LibraryBranch)  
- `hasAvailabilityStatus` (Copy → AvailabilityStatus)  
- `hasAccessibilityFeature` (Copy → AccessibilityFeature)  

---

## Key Data Properties

- `hasTitle`  
- `publicationYear`  
- `barcodeID`  
- `copyNumber`  

Domains and ranges were explicitly defined to ensure structural correctness and reasoning compatibility.

---

## Reasoning & Validation

The ontology was validated using the **HermiT reasoner** to:

- Confirm logical consistency  
- Support inferred classification  
- Validate domain and range constraints  
- Enable semantic query results  

---

## Example Semantic Queries (DL Query)

The ontology supports structured reasoning queries such as:

**Retrieve all copies with Large Print accessibility:**

**Retrieve all Fiction books:**

These examples demonstrate how semantic constraints enable more precise and explainable retrieval compared to keyword-based search systems.

---

## Strengths of the Design

- Clear separation between **Book (abstract work)** and **Copy (physical instance)**  
- Operational modelling of availability and circulation states  
- Accessibility-aware search capability  
- Branch-aware inventory representation  
- Logical consistency verified through reasoning  
- Extensible structure for reservations, fines, or recommendation logic  

---

## Limitations & Future Improvements

- Integration with a live database or SPARQL endpoint would be required for deployment  
- Natural language query interpretation would require an NLP layer  
- Scalability considerations would arise with real-world catalogue size  

---

## Repository Structure

- ontology/ → OWL ontology file
- screenshots/ → Class hierarchy, properties, reasoning, DL queries
- docs/ → Full project report
- reflection.md → Design reflection and extension ideas


---

## Technologies Used

- Protégé  
- OWL (Web Ontology Language)  
- Description Logic  
- HermiT Reasoner  

---

## Author

Oghenevurie Lauretta  
MSc Artificial Intelligence
