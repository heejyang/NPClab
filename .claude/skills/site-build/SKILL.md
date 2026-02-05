---
name: site-build
description: Build and test the NPClab Jekyll site locally
disable-model-invocation: true
allowed-tools: Bash
---

Build and test the NPClab site:

1. **Clear Jekyll cache**: Delete .jekyll-cache/ and _site/ directories
2. **Start Docker**: Run `docker compose up` to build and serve locally
3. **Verify**: Check that site is accessible at http://localhost:8080
4. **Check console**: Look for any build errors or warnings

If issues occur:
- Check _config.yml syntax
- Verify all referenced files exist (PDFs, images)
- Check BibTeX formatting in _bibliography/papers.bib
- Review git status for uncommitted changes

Report build status and any errors found.
