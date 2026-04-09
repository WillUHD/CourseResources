# Contributing to CourseResources

### Common Course DSL file format specification
- The Common Course language is defined as a dialect of JSON that enables full-line comments.
- Comments are defined by the regex `^\s*\/\/.*` (regex used for easy parsing in programs)
- In words: full-line comments span a whole line, starting with any amount of whitespace, and then immediately after, `//`.
- Files that follow the Common Course can have any convenient suffix (it doesn't matter). Usually, the extension is something that the file itself (or the service using it) does (such as `.gpa`, `.catalog`).
- If your app caches the data in any way, the best practice is to cache as-is (not a modified version with comments and license removed) in order to respect author credits, and then re-parse on the fly. 
- Example:
  ```CommonCourse
  // this comment is OK.
        // you can insert an arbitrary amount of whitespace before
        // which is nice for indentation
  {"courseVersion": "alpha 0.1"}, // this is ILLEGAL! NOT ok!
  {"tracks": ["AP", "IB", "ASA2"]} // please don't write comments like this!
  ```
- Use this regex in code: `^\s*\/\/.*`

### JSON best practices
- The preferred style is a "hybrid-compact human-readable JSON with cuddled brackets"
- The goal is a high-density, human-readable format that minimizes vertical & horizontal line stress (but mainly vertical) by bridging delimiters (similar? to TOON). You can find examples all in this repo here!
- Specific styling:
  - Never place a closing bracket on its own line if another item follows it - do it like `], "10": [` or `}, {`
  - Only expand primary object properties (like `id`, `name`, `description`) onto new lines
  - Simple nested structures (like single-element arrays) remain on a single line unless they exceed a general rule of thumb for horizontal complexity or length
  - Minimize vertical whitespace by trailing the opening bracket of a new object or array immediately after the previous one's closing bracket
  - Ensure the first property of a nested object starts on the same line as the opening brace to keep the block tight

### FAQs
- **wHy nO inLiNe cOmMeNtS?!?**
  - Sorting inline comments will become slow to parse, especially for files that have thousands of lines.
  - It is a design choice to not support inline comments, because it's also complex to solve for edge cases inside strings, nested strings, escaped quotes, and string blocks.
  - We think having full-line comments is enough to get the point across of what an inline comment would do.
  - PLEASE do not PR any related projects with aigc bug fixes claiming to add inline support. It's not planned for the specification.
- **wHy nOt JSONc oR yAML ?!?** Requires extra, non-native dependencies especially for Swift. The project originally had no dependencies so I don't want the rework to bloat everything up.
