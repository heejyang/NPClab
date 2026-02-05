---
name: publication-check
description: Check BibTeX publications in papers.bib for completeness and formatting issues
---

When checking publications, verify:

1. **Required Fields**: Each BibTeX entry has title, author, year, journal/booktitle
2. **File References**: If pdf field exists, verify the file exists in assets/pdf/
3. **URLs**: Check that code, website, arxiv, doi links are properly formatted
4. **Author Names**: Ensure author names follow consistent formatting
5. **Year Sorting**: Verify entries are properly organized by year

Report any issues found and suggest fixes.

If $ARGUMENTS is provided, only check entries matching that pattern (e.g., year, author name).
