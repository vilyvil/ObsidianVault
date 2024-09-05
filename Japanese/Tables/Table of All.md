```dataview
TABLE meaning, connection
FROM #vocab or #kanji or #radical 
WHERE file.name != "KanjiTemplate"
WHERE file.name != "RadicalTemplate"
WHERE file.name != "VocabTemplate"
```
