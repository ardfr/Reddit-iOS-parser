**Reddit iOS Chat Parser**
The RedditAppParser is a command-line forensic tool designed to extract and analyse Reddit iOS chat artefacts from application cache data.

It processes Matrix-style chat data stored within the Reddit iOS application directories and generates structured outputs for forensic analysis.

**Input Data Structure**
The tool expects the root folder containing subdirectories extracted from:
APP GUID\Library\Caches\MatrixChat\roomsAccount\<UNIQUE_ID>\
Where:
<UNIQUE_ID> is a hash-like identifier (example below)
Example:
62663babbf0b09d98e667e136ed571bc56b2552d20e79e1ffb8a9ac08c768faf

**Expected Folder Layout**
Inside the <UNIQUE_ID> directory, the following subfolders should be present:
Account-*
Downloads-*
MatrixUsers-*
Uploads

Example:
Account-37
Downloads-6
MatrixUsers-6
Uploads

**Features**
Extraction of Reddit chat messages
Parsing of Matrix-style event data
JSON content decoding
Timestamp conversion
Structured output generation (CSV / HTML)
Cross-referencing users and messages

**Usage**
Basic Command
**RedditAppParser.exe --root-folder ROOT_FOLDER --out-dir OUT_DIR**
Example
RedditAppParser.exe --root-folder "D:\Evidence\Reddit\roomsAccount\62663babb..." --out-dir "D:\O

**Arguments**
Argument	Description
--root-folder	Path to folder containing subfolders (Account-*, Downloads-*, etc.)
--out-dir	Output directory where reports will be generated
