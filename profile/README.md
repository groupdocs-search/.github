<h1 align="center">GroupDocs.Search</h1>

<h3 align="center">Full-Text Search API for 80+ Document Formats</h3>

<p align="center">
  <strong>GroupDocs.Search</strong> is an on-premise full-text search API that indexes PDF, Word, Excel, PowerPoint, email, eBook, archive and image files and searches them with keyword, phrase, wildcard, regular-expression, fuzzy, boolean, faceted, synonym and homophone queries - then highlights what it found. SDKs for .NET, Java, Node.js and Python.
</p>

[![Product Page](https://img.shields.io/badge/Product%20Page-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.com/search/)
[![Docs](https://img.shields.io/badge/Docs-2865E0?style=for-the-badge&logo=Hugo&logoColor=white)](https://docs.groupdocs.com/search/)
[![Demos](https://img.shields.io/badge/Demos-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.app/search/family)
[![API](https://img.shields.io/badge/API-2865E0?style=for-the-badge&logo=html5&logoColor=white)](https://reference.groupdocs.com/search/)
[![Blog](https://img.shields.io/badge/Blog-2865E0?style=for-the-badge&logo=WordPress&logoColor=white)](https://blog.groupdocs.com/category/search/)
[![Search](https://img.shields.io/badge/Search-2865E0?style=for-the-badge&logo=searchengin&logoColor=white)](https://search.groupdocs.com/)
[![Support](https://img.shields.io/badge/Support-2865E0?style=for-the-badge&logo=Discourse&logoColor=white)](https://forum.groupdocs.com/c/search)
[![Temp License](https://img.shields.io/badge/Temp%20License-2865E0?style=for-the-badge&logo=rocket&logoColor=white)](https://purchase.groupdocs.com/temporary-license)

## Latest Search News & Updates
* **NEW:** [GroupDocs.Search for Python via .NET 26.10](https://pypi.org/project/groupdocs-search-net/) on PyPI, the first Python release: engine 26.10 with the .NET 10 runtime embedded, Python 3.5 - 3.14 on Windows, Linux and macOS (Intel and Apple Silicon), the engine's events as Python handlers, and custom text extractors, loggers and OCR connectors as plain Python objects. [Release notes](https://releases.groupdocs.com/search/python-net/release-notes/).
* Published [GroupDocs.Search 26.10](https://www.nuget.org/packages/GroupDocs.Search/) for .NET on NuGet: a new index format that needs about half the memory, opens 2 - 4 times faster and applies every change atomically; `IndexUpdater` converts indexes made by versions 22.7 - 26.8. [Migration notes](https://docs.groupdocs.com/search/net/migration-notes/).
* Published GroupDocs.Search 26.9.1 for Java on the [GroupDocs Maven repository](https://releases.groupdocs.com/java/repo/): a new index format, to which `IndexUpdater` upgrades indexes made by versions 22.7 - 25.4, HTML extracted by the engine itself, and fixes for merging large indexes and deleting documents. [Release notes](https://releases.groupdocs.com/search/java/release-notes/).
* The [GroupDocs.Search MCP server](https://docs.groupdocs.com/search/mcp/) 26.10 lets AI agents index a folder and search it **locally**, and ships as a Docker image.

## Supported Platforms & Repository Groups

### .NET Document Search (C#, ASP.NET, WinForms)
Index and search PDF, Office, email, eBook, archive and image files on .NET Framework 4.6.2+, .NET Core 3.0+ and .NET 5 and later.
* **[GroupDocs.Search-for-.NET](https://github.com/groupdocs-search/GroupDocs.Search-for-.NET)**: API examples for indexing, search options, highlighting, dictionaries and search networks.

```csharp
using System;
using GroupDocs.Search.Results;

// Create an index in a folder and add the documents of another folder
// (GroupDocs.Search.Index, not System.Index)
var index = new GroupDocs.Search.Index(@"c:\MyIndex");
index.Add(@"c:\MyDocuments");

// Search the index and list the documents found
SearchResult result = index.Search("Einstein");
for (int i = 0; i < result.DocumentCount; i++)
{
    FoundDocument document = result.GetFoundDocument(i);
    Console.WriteLine(document.DocumentInfo.FilePath + ": " + document.OccurrenceCount);
}
```

### Java Document Search (Maven, Spring)
Native Java library for indexing and searching PDF, Office, email, eBook, archive and image files.
* **[GroupDocs.Search-for-Java](https://github.com/groupdocs-search/GroupDocs.Search-for-Java)**: Java examples; the package `com.groupdocs:groupdocs-search` comes from the [GroupDocs Maven repository](https://releases.groupdocs.com/java/repo/).

```java
import com.groupdocs.search.Index;
import com.groupdocs.search.results.FoundDocument;
import com.groupdocs.search.results.SearchResult;

// Create an index in a folder and add the documents of another folder
Index index = new Index("c:/MyIndex");
index.add("c:/MyDocuments");

// Search the index and list the documents found
SearchResult result = index.search("Einstein");
for (int i = 0; i < result.getDocumentCount(); i++) {
    FoundDocument document = result.getFoundDocument(i);
    System.out.println(document.getDocumentInfo().getFilePath() + ": " + document.getOccurrenceCount());
}
```

### Node.js Document Search (Node.js via Java)
Add full-text search to Node.js services and scripts with the Java engine.
* **[GroupDocs.Search-for-Node.js-via-Java](https://github.com/groupdocs-search/GroupDocs.Search-for-Node.js-via-Java)**: Node.js examples; install with `npm install @groupdocs/groupdocs.search`.

```javascript
const groupdocs = require('@groupdocs/groupdocs.search');

// Create an index in a folder and add the documents of another folder
const index = new groupdocs.Index('c:/MyIndex');
index.add('c:/MyDocuments');

// Search the index and list the documents found
const result = index.search('Einstein');
for (let i = 0; i < result.getDocumentCount(); i++) {
  const document = result.getFoundDocument(i);
  console.log(document.getDocumentInfo().getFilePath() + ': ' + document.getOccurrenceCount());
}
```

### Python Document Search (Python via .NET)
A self-contained Python package with the .NET runtime embedded: `pip install groupdocs-search-net`, Python 3.5 - 3.14.
* **[GroupDocs.Search-for-Python-via-.NET](https://github.com/groupdocs-search/GroupDocs.Search-for-Python-via-.NET)**: Runnable examples for every documented scenario, with a Dockerfile.
* [PyPI](https://pypi.org/project/groupdocs-search-net/) | [Docs](https://docs.groupdocs.com/search/python-net/) | [API Reference](https://reference.groupdocs.com/search/python-net/) | [Release Notes](https://releases.groupdocs.com/search/python-net/release-notes/)

```python
from groupdocs.search import Index

# Create an index in a folder and add the documents of another folder
index = Index("./MyIndex")
index.add("./MyDocuments")

# Search the index and list the documents found
result = index.search("Einstein")
for document in result:
    print(document.document_info.file_path, document.occurrence_count)
```

### MCP Server for AI Agents (Claude, Cursor, Copilot)
Let AI agents index a folder of documents and search it **locally over MCP**: nothing is uploaded, and the index stays on disk for the next question.
* **[GroupDocs.Search.Mcp](https://github.com/groupdocs-search/GroupDocs.Search.Mcp)**: The MCP server: index a folder, search it by content, quote the matching passages, and keep the index current.
* **[GroupDocs.Search.Mcp.Tests](https://github.com/groupdocs-search/GroupDocs.Search.Mcp.Tests)**: Integration suite that verifies every published release.

```bash
# Run the server with your documents mounted, then ask your agent:
docker run --rm -i -v $(pwd)/documents:/data ghcr.io/groupdocs-search/search-net-mcp:latest
```

> "Index the contracts folder, then tell me which contracts mention a termination penalty and quote the clause."

[MCP documentation](https://docs.groupdocs.com/search/mcp/) | [Docker](https://github.com/orgs/groupdocs-search/packages/container/package/search-net-mcp)

## Business Use-Cases
- Enterprise content search across mixed formats, with OCR for scanned documents and images.
- Compliance and legal discovery: highlight hits, filter by metadata, and export the text found.
- Knowledge bases and customer support search with typo-tolerant and synonym search.
- E-discovery and audit: date and number range queries, faceted search and filtering.
- Retrieval for AI pipelines: find the documents and quote the passages an agent needs.
- Media libraries: reverse image search over indexed image hashes.

## API Key Features & Benefits
- 80+ formats, OCR-backed text extraction, metadata indexing, and custom text extractors.
- Indexes in memory or on disk; update, merge, optimize and repair them, and convert old ones.
- Search modes: simple, boolean, regular expression, fuzzy, wildcard, phrase with wildcards, faceted.
- Spell checking, keyboard layout correction, homophone, synonym and word-form search.
- Indexing control: stop words, blended characters, character replacements, document filters, passwords.
- Events for progress, errors and passwords; asynchronous indexing; search networks across machines.
- Highlighting of whole documents or fragments, in HTML or plain text.

## Getting Started
- .NET: `dotnet add package GroupDocs.Search`
- Java: add `com.groupdocs:groupdocs-search` from the GroupDocs repository, `https://releases.groupdocs.com/java/repo/`
- Node.js: `npm install @groupdocs/groupdocs.search`
- Python: `pip install groupdocs-search-net`
- Run the sample projects from the repositories above to index documents and execute search queries.

## Technical Support & Resources
- Documentation and tutorials: https://docs.groupdocs.com/search/
- Free support forum: https://forum.groupdocs.com/c/search
- Temporary license for full-feature evaluation: https://purchase.groupdocs.com/temporary-license

## Tags

`groupdocs-search` `document-indexing` `full-text-search` `search-text-in-document` `create-text-index` `regex-search` `fuzzy-search` `synonym-search` `ocr-search` `reverse-image-search` `enterprise-search` `python` `mcp` `mcp-server` `ai-agents`
