<h1 align="center">GroupDocs.Search</h1>

<p align="center">
  GroupDocs.Search delivers enterprise-grade full-text search, document indexing, and text extraction to help teams create a fast, accurate search experience across PDFs, Office files, images (OCR), emails, archives, and more. Build end-user search features, create text indexes for quick document search, and keep results fresh with high-performance index updates.
</p>

[![Product Page](https://img.shields.io/badge/Product%20Page-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.com/search/)
[![Docs](https://img.shields.io/badge/Docs-2865E0?style=for-the-badge&logo=Hugo&logoColor=white)](https://docs.groupdocs.com/search/)
[![Demos](https://img.shields.io/badge/Demos-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.app/search/family)
[![API](https://img.shields.io/badge/API-2865E0?style=for-the-badge&logo=html5&logoColor=white)](https://apireference.groupdocs.com/search/)
[![Blog](https://img.shields.io/badge/Blog-2865E0?style=for-the-badge&logo=WordPress&logoColor=white)](https://blog.groupdocs.com/category/search/)
[![Search](https://img.shields.io/badge/Search-2865E0?style=for-the-badge&logo=searchengin&logoColor=white)](https://search.groupdocs.com/)
[![Support](https://img.shields.io/badge/Support-2865E0?style=for-the-badge&logo=Discourse&logoColor=white)](https://forum.groupdocs.com/c/search)
[![Temp License](https://img.shields.io/badge/Temp%20License-2865E0?style=for-the-badge&logo=rocket&logoColor=white)](https://purchase.groupdocs.com/temporary-license)

## Latest Search News & Updates
- Recent updates improve OCR-backed indexing, faster spell correction, and refined fuzzy search defaults.
- New guidance on distributed search networks and image-hash indexing for reverse image search.
- Expanded examples for regular expressions, homophone search, and keyboard layout correction.

## Supported Platforms & Repository Groups

### .NET Document Indexing & Search (C#, ASP.NET, WinForms)
High-performance APIs for full-text search, indexing, and highlighting on .NET Framework and .NET Core.
- **GroupDocs.Search-for-.NET**: Core API for indexing, spell check, fuzzy/regex/boolean search.  
  Repository: https://github.com/groupdocs-search/GroupDocs.Search-for-.NET
- **Showcases**: ASP.NET MVC UI demonstrating search and highlighting.  
  Examples: https://github.com/groupdocs-search/GroupDocs.Search-for-.NET/tree/master/Showcases/GroupDocs.Search-UI

```csharp
string indexFolder = @"c:\MyIndex\";
string documentsFolder = @"c:\MyDocuments\";

// Create index and add documents
Index index = new Index(indexFolder);
index.Add(documentsFolder);

// Regular expression search: two or more identical chars at word start
SearchResult result = index.Search("^^(.)\\1{1,}");
```

### Java Document Indexing & Search (Maven, Spring)
Native Java API for indexing, fuzzy search, regex search, and OCR-backed text search.  
Repository: https://github.com/groupdocs-search/GroupDocs.Search-for-Java

```java
com.groupdocs.search.Index index = new com.groupdocs.search.Index("indexDir");
index.add("docsDir");
com.groupdocs.search.results.SearchResult result =
    index.search("keyboard layout correction", new com.groupdocs.search.options.SearchOptions());
```

### Python & Node.js via .NET/Java
Cross-platform bindings to integrate full-text search into scripting and server workflows.  
Repositories: 
- Python via .NET: https://github.com/groupdocs-search/GroupDocs.Search-for-PythonNet  
- Node.js via Java: https://github.com/groupdocs-search/GroupDocs.Search-for-Node.js-via-Java

## Business Use-Cases
- Enterprise content search across mixed formats with text indexing and OCR.
- Compliance & legal discovery: highlight hits, export results, filter by metadata.
- Knowledge bases & customer support search with typo-tolerant and synonym search.
- E-discovery and audit: date/number range queries, faceted search, and filtering.
- Media libraries: reverse image search using indexed image hashes.

## API Key Features & Benefits
- 80+ formats, OCR-backed text extraction, metadata indexing, and custom extractors.
- Create text indexes in memory or on disk; update, merge, optimize, and compact indexes.
- Flexible search modes: simple, boolean, regex, fuzzy, wildcard, phrase with wildcards, faceted search.
- Spell check, keyboard layout correction, homophone search, and synonym search.
- Indexing controls: stop words, blended characters, whole-word characters, character replacement.
- Distributed search network support for load-balanced queries across indexes.
- Save extracted text with configurable compression; filter documents during indexing.
- Highlight results per document or per segment; search across multiple indexes simultaneously.

## Getting Started
- .NET: `Install-Package GroupDocs.Search` or `dotnet add package GroupDocs.Search`
- Java: Add the GroupDocs.Search dependency from Maven Central.
- Run sample projects from the repositories above to index documents and execute search queries.

## Technical Support & Resources
- Documentation and tutorials: https://docs.groupdocs.com/search/
- Free support forum: https://forum.groupdocs.com/c/search
- Temporary license for full-feature evaluation: https://purchase.groupdocs.com/temporary-license

## Tags
`groupdocs-search` `document-indexing` `full-text-search` `search-text-in-document` `create-text-index` `quick-document-search` `regex-search` `fuzzy-search` `synonym-search` `ocr-search` `reverse-image-search` `enterprise-search` `metadata-search` `spell-check-search`
