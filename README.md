# 🏛️ Auction House Database

A relational database system for an online auction platform, built as part of the Database Systems course at **Grenoble INP - Ensimag**. Includes full schema design, SQL implementation on Oracle, and a Java/JDBC demonstrator application.

## Overview

The project models the backend for **Baie-Électronique**, a company running online product auctions. Users can list products for sale, and bid on others' listings across configurable auction types:

- **Ascending or descending auctions**: bids increase over time, or price drops until someone commits
- **Single-bid or multi-bid rules**: limit users to one offer per product, or allow repeated bidding
- **Time-limited or open-ended**: fixed end date, or a 10-minute inactivity cutoff
- **Revocable or firm sales**: auctions can be cancelled if the reserve price isn't met

## What this covers

- **Entity-Relationship modeling**: full analysis of functional dependencies, value constraints, multiplicity constraints, and contextual business rules
- **Relational schema translation**: E/R diagram translated into normalized relations, with justified normal forms
- **Transactional SQL**: concurrency-safe transactions for room creation, bidding, and auction resolution - tested on Oracle for concurrent access correctness
- **Java/JDBC demonstrator**: a text-based interface exercising the core functionalities (create a sale room, place a bid, determine auction winners)

## Tech stack

Oracle SQL · Java · JDBC

## Project structure

```
App/
├── tables.sql → Schema creation (DDL)
├── populate.sql → Sample data
├── Offer.sql → Bidding-related queries/transactions
├── src/Main.java → JDBC demonstrator entry point
```
