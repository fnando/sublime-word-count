## Description

Provides a real-time Word Count and character count in the status-bar for
Sublime Text. See: http://www.sublimetext.com/

Count words and/or characters on document or in selections. By default,
whitespace is not included in the character count.

The minimal word length is 1 and does not count digits.

An estimated reading time is now appended to the end of the word count.

## Installation

### Setup Package Control Repository

1. Follow the instructions from https://sublime.fnando.com.
2. Open the command pallete, run “Package Control: Install Package“, then search
   for “WordCount“.

### Git Clone

Clone this repository into the Sublime Text “Packages” directory, which is
located where ever the “Preferences” -> “Browse Packages” option in sublime
takes you.

## Preferences

Located under Sublime Text>Preferences>Package Settings>Settings — User
(You probably need to copy the default settings from the uneditable Sublime
Text>Preferences>Package Settings>Settings — **Default**)

- `enable_live_count` : Default is `true`. Allows to control if the live word
  counter is enabled. Otherwise will be enabled for selections only.
- `enable_readtime` : Default is `false`. Allows you to control if the estimated
  reading time is enabled. Reading time is only displayed when there is a time >
  1s.
- `readtime_wpm` : Default is `200`. Sets the WPM to calculate the Estimated
  Reading Time for the file.
- `allowed_syntaxes` : Default is `[]`. An array of syntax names that WordCount
  should run on. Example: `["Plain text", "Markdown"]`. If the array is empty,
  like it is by default, WordCount will run on any syntax.
- `rejected_syntaxes` : Default is
  `["CSS", "SQL", "JavaScript", "Python", "PHP", "JSON"]`. An array of syntax
  names that WordCount should not run on. If the array is empty, WordCount will
  run on any syntax.
- `char_ignore_whitespace` : Default is `true`. Whether to skip whitespace for
  the character count.
- `enable_line_word_count` : Default is `false`. Display the count of words
  found on current line.
- `enable_line_char_count` : Default is `false`. Display the count of characters
  found on current line.
- `enable_count_lines` : Default is `false`. Display the number of lines in
  file.
- `enable_count_chars` : Default is `false`. Display the number of characters in
  file.
- `enable_count_pages` : Default is `true`. Display the number of pages in file.
- `page_count_mode_count_words` : Default is `true`. Sets the page count mode to
  words per page.
- `words_per_page` : Default is `300`. Sets the number of words per page used to
  calculate number of pages.
- `word_regexp` : Word Regular expression. Defaults empty, an internal regular
- expression is used. If the portion of text matches this RegExp then the word
- is counted.
- `word_split` : Split portions of text to test later as words with a Regular
  expression. Defaults to String.split() with no arguments, means that content
  will trim() and empty values (all whitespaces) are not used. In case of
  containing some value different than empty, the return of "re.findall" will be
  used.
- `split`: Default is `{"php": ["<[^>]*>"], "html": ["<[^>]*>"]}`. Remove regex
  patterns by syntax. Use lowercase for the syntax names.

## Inspiration

- The main loop inspired by [sublimelint](https://github.com/lunixbochs/sublimelint)
- The count inspired by the original [WordCount plugin](http://code.google.com/p/sublime-text-community-packages/source/browse/#svn%2Ftrunk%2FWordCount) committed by mindfiresoftware.

## Contributors

- Liam Cain
- Lee Grey
- Hawken Rives
- Yaw Anokwa
- James Brooks
- Antony Male
- Alex Galonsky
- RikkiMongoose
- ChrisJefferson
- Harry Ng. (From [Word Count Tool](http://wordcounttools.com/))
- MangleKuo
- Nick Cody
- Amanda Neumann
