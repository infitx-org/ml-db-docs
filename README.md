# ml-db-docs

## Prerequisites

Database documentation generator [tbls](https://github.com/k1LoW/tbls).

Install tbls:
```bash
brew install tbls
```

## Usage

### 1. Generate Database Documentation

Generate markdown documentation from your database schema:
```bash
tbls doc
```

### 2. Convert to PDF

Convert the generated markdown files to PDF format:
```bash
node scripts/mdToPdf.js
```

### 3. Generate ERD Diagrams

Create entity relationship diagrams from the tbls-generated JSON schema:
```bash
npx @liam-hq/cli erd build \
  --input docs/central_ledger/schema.json \
  --format tbls \
  --output-dir dist/central_ledger
```

**Note:** Replace `central_ledger` with your specific database name/path as needed.