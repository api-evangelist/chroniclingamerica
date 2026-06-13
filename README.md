# Chronicling America

Chronicling America is a Library of Congress initiative providing free public access to a searchable database of historic American newspaper pages from 1770 to 1963. The platform hosts over 20 million digitized newspaper pages from hundreds of US newspapers contributed by institutions in the National Digital Newspaper Program (NDNP). The API requires no authentication and returns responses in JSON and Atom feed formats.

**Provider:** Library of Congress  
**Base URL:** https://chroniclingamerica.loc.gov  
**Authentication:** None required  
**Cost:** Free  

## APIs

| API | Description |
|-----|-------------|
| Search API | Full-text search across 20M+ historic newspaper pages by keyword, date, state, and title |
| Titles API | Bibliographic metadata for newspaper titles by LCCN, including issue and batch listings |
| Pages API | Individual page records with OCR text, IIIF image URLs, PDF, JP2, and TIFF downloads |

## Key Endpoints

- `GET /search/pages/results/?andtext={query}&format=json` — Full-text page search
- `GET /newspapers.json` — All newspaper titles in the collection
- `GET /lccn/{lccn}.json` — Metadata for a specific newspaper title
- `GET /lccn/{lccn}/issues.json` — All issues for a newspaper title
- `GET /lccn/{lccn}/{date}/ed-{edition}/seq-{sequence}.json` — Individual page record
- `GET /lccn/{lccn}/{date}/ed-{edition}/seq-{sequence}/ocr.txt` — OCR text for a page
- `GET /batches.json` — All ingestion batches in the collection
- `GET /batches/{batch_name}.json` — Pages in a specific batch

## Resources

- [API Documentation](https://chroniclingamerica.loc.gov/about/api/)
- [Collection Overview](https://chroniclingamerica.loc.gov/about/)
- [LOC Labs Bulk Data](https://labs.loc.gov/work/experiments/bulk-data/)
- [National Digital Newspaper Program](https://www.loc.gov/ndnp/)
- [Library of Congress Legal](https://www.loc.gov/legal/)
