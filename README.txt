MESA ARCHIVE: Nupur Gulgulia, PGP Cohort IV (Batch 2027), Mesa School of Business
==============================================================================

This folder is a complete local copy of everything archived from the Nexus LMS
(students.mesaschool.co.in). It is the same content as the private cloud bucket "mesa-files"
(Neon project mesa-archive), with the same folder paths. It needs no app to be useful:
every file opens with normal software.

WHAT IS WHERE
  Pre-Term/, Term 1/, Term 2/
      <Course>/<Tab>/<Folder>/<file>
      Course material exactly as it appeared on Nexus (PDF, PPTX, DOCX, XLSX, PNG).
      Items that were notes or links on Nexus are saved as  <name>.note.json :
        a small text file with the note's text and the links it pointed to.
  _links/
      Copies of the content BEHIND those links, saved while access still worked:
        gdoc/, gslide/   Google Docs / Slides exported as PDF   (file name = Google file id)
        gsheet/          Google Sheets exported as XLSX
        gdrive_file/     Google Drive files (original format), one folder per file id
        gdrive_folder/   Google Drive folders; _index.json lists the files inside
        gamma/           Gamma decks (text only; Gamma does not allow file export)
      To find which course a link belongs to, search the .note.json files for the file id.
  _ocr/
      Text recognised (OCR) from scanned PDFs that had no text layer.
      OCR text can contain errors and loses formatting (e.g. bold answers in answer keys).
  _meta/capture/
      The full crawl of Nexus (every item, with Nexus material ids) used to verify this archive.

NOT IN THIS FOLDER
  - Class recordings: they are YouTube links (in the app's database and in note files),
    not video files.
  - Grades: none were published on Nexus at the time of capture.

INTEGRITY
  SHA256SUMS.txt holds a SHA-256 checksum for every file. To verify the whole archive
  (Git Bash / Linux / macOS):     sha256sum -c SHA256SUMS.txt
  _archive_index.json maps every bucket key to its local path, size, MD5 and SHA-256.

  First complete verified copy: 20 Oct 2026 (479 files, 953 MB, all checksums OK).
  The archive is refreshed by:  node scripts/mirror-local.js   (in the mesa-handoff project)
