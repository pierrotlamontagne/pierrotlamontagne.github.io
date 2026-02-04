# BibTeX files for publications

Put one `.bib` file per publication here. Each file should contain a single BibTeX entry that visitors can copy to cite your work.

**Linking a publication to its BibTeX:** In the publication’s front matter (in `_publications/YYYY-MM-DD-title.md`), set:

```yaml
biburl: '/files/bib/yourkey.bib'
```

The "BibTeX" link on the publications page will point to this file so users can open or copy the entry.

**Adding a new paper:** Create a new `.bib` file in this folder (e.g. `author2025shorttitle.bib`) with the full BibTeX entry, then add the `biburl` line above to the corresponding file in `_publications/`.
