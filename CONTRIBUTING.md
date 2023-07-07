# covidat-data data guidelines

Data MUST fit these criteria:

1. No leaks! ⚠ The data must have been intentionally available to the public
  at some point. This is a hard rule.
2. The data must be related to the areas listed in [the README](./README.md).

Data should fit these criteria to be included:

3. Data must originate from official or quasi-official sources
   (Statistik Austria, government, GÖG, ...).
4. The most interesting data for this repository is data that is only 
  temporarily available from the original source, e.g. when only data for the most recent year/month/etc. is kept online, or when the time series is 
  regularly revised and the pre-revision data is of interest (it usually 
  is) and not kept online (it usually isn't).
5. Data should be machine-readable or at least contain numeric data
  that can be manually translated.
6. CSV > XML/JSON/etc > XLSX > HTML > PDF, though we can't choose anyway in most
   cases.
7. Not already archived by another trusted source.

## Changing data

For changing data, follow these rules:

1. The only allowed changes to any data file in this repository is (logical) append.
   No overwrites must occur and it should be clear how much was appended
   (e.g. daily / monthly / yearly append).
2. Otherwise and by default,
   one separate file per update should be stored and the timestamp
   should be encoded in the filename. If this isn't the case in the original
   filename, use the suffix `_%Y%m%d_%H%M%S` before the file extension
   (this is in
   [C/Python strftime format](https://docs.python.org/3.11/library/datetime.html#strftime-and-strptime-format-codes), an example suffix
   could be `_20230431_2355959`, all parts are left-padded with zero).
   1. Both UTC or the original timezone (usually Vienna) are OK.
      Unless otherwise documented, UTC is assumed.
   2. The timestamp should encode the creation, or HTTP Last-Modified timestamp
      of the file (in that order of preference). If none of that is known, the
      download date (preferably from the server's `Date` header) should be used.
      Do not use any logical timestamp that would potentially stay the same for
      new revisions of the file.

## Large files

Git and GitHub are not really designed for storing large or non-text data,
which is what this repository does. For large files in particular, see
<https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github>.

You may be able to compress the data file to make it smaller, this often works
incredibly well for large text files (e.g. XML). Compressing multiple files
together with a suitable archive format (e.g., tar.xz or 7z but not zip)
is especially efficient. The default archive formats (if the data is not
already using a different archive format in the original) are .xz (LZMA) and
.tar.xz as they are widely implemented and achieve good compression ratios.

If the file is still too large or not compressible,
the file can be attached to a GitHub release.

If it is also too large for that it is probably not suited for this repository.

Since releases can't be contributed using PRs and issue attachments have a much smaller size limit, please create an issue and if the file is interesting
enough, we'll find a way (Dropbox link, etc.).

If sensible, a set of large files should be bundled into a single release
(but usually large files should be bundled into a single .tar.xz archive
to minimize the size).

Any such release must be linked from the README.md of this repository.

## Auxiliary files

Additional metadata or documentation files describing the data are welcomed.
Scripts or other code for any purpose or in any form is out of scope
(we'll be pragmatic about snippets in doc files, no need to go out of your
way if what you want to describe is really best described in code).

Some files were downloaded with a script that stores HTTP headers in a file
`<original_name_without_extension>_hdr.txt` using the format of Python's
[`email.message.EmailMessage.as_bytes`](https://docs.python.org/3.11/library/email.message.html#email.message.EmailMessage.as_bytes).
This is a nice-to-have for any file downloaded via HTTP but not required in any way.

It is particularly useful to document the original URL of your file.
