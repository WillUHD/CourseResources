# Contributing to GPAResources

### Common Course DSL file format specification
- The Common Course language is defined as a dialect of JSON that enables full-line comments.
- Comments are defined by the regex `^\s*\/\/.*` (regex used for easy parsing in programs)
- In words: full-line comments span a whole line, starting with any amount of whitespace, and then immediately after, `//`.
- **wHy nO inLiNe cOmMeNtS?!?**
  - Sorting inline comments will become slow to parse, especially for files that have thousands of lines.
  - It is a design choice to not support inline comments, because it's also complex to solve for edge cases inside strings/quotes, nested strings, or string blocks.
  - We think having full-line comments is enough to get the point across of what an inline comment would do. PLEASE do not PR any related projects with aigc bug fixes claiming to add inline support. It's not planned for the specification.
- Files that follow the Common Course can have any convenient suffix (it doesn't matter). Usually, the prefix is something that the file itself (or the service using it) does (such as `.gpa`, `.catalog`).
- As a best practice (currently), insert the license boilerplate at the end of the file. It's weird and may change in the future. 
- Example:
  ```CommonCourse
  // this comment is OK.
        // you can insert an arbitrary amount of whitespace before
        // which is nice for indentation
  {"courseVersion": "alpha 0.1"}, // this is ILLEGAL! NOT ok!
  {"tracks": ["AP", "IB", "ASA2"]} // please don't write comments like this!
  ```
- Use this regex in code: `^\s*\/\/.*`

