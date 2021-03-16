A USFM stylesheet is a text file named using an `.sty` extension which contains a collection of definitions and properties for USFM markers. These properties are typically used for expressing information about marker identification and description, the location and order in which markers can occur within a USFM file, and for expressing formatted display preferences. Stylesheets were originally developed for use by the Paratext scripture translation editor, but they could be of use in other contexts as well. They provide a rudimentary grammar to USFM and as such are also maintained in this repository.

## Stylesheet Properties

Entries in a USFM stylesheet can contain the following properties. All of these are optional except: `\Marker`, `\Name`, and `\StyleType`.

**Property:** `\Bold`  
**Example:** `\Bold`  
**Description:** Text is bold.

**Property:** `\Color`  
**Example:** `\Color 8421504`  
**Description:** RGB color values. See Commonly Used Color Values section below.

**Property:** `\Description`  
**Example:** `\Description Poetry text, level 1 indent`  
**Description:** A comment describing this marker. Insert the text "(basic)" at the end of the description to cause this marker to be listed with the "basic" markers at the start of the style selection list.

**Property:** `\Endmarker`  
**Example:** `\Endmarker f*`  
**Description:** End marker, if any, corresponding to this marker.

**Property:** `\FirstLineIndent`  
**Example:** `\FirstLineIndent .125`  
**Description:** Amount of extra indent given to first line of paragraph in inches.

**Property:** `\Fontname`  
**Example:** `\Fontname Courier New`  
**Description:** Name of font used to display text for this marker. If you don't specify a font in the stylesheet the program will default to the font specified for the language.

**Property:** `\FontSize`  
**Example:** `\FontSize 20`  
**Description:** Size of font in points. The sizes of the font specified in the stylesheet are automatically adjusted relative to the size of the font specified in the Language settings. The default relative size is 12. Therefore if the Language settings specify a font size of 14, any fonts sizes specified in the stylesheet will be adjusted upwards by two points.

**Property:** `\Italic`  
**Example:** `\Italic`  
**Description:** Font for this tag is italicized.

**Property:** `\Justification`  
**Example:** `\Justification right`  
**Description:** Justification for this paragraph: left, center, right, both.

**Property:** `\LeftMargin`  
**Example:** `\LeftMargin .75`  
**Description:** Amount of indent given to this paragraph in inches.

**Property:** `\LineSpacing`  
**Example:** `\LineSpacing 2`  
**Description:** Amount of extra space between lines in this paragraph in points. 0 = single space, 1 = space and a half, 2 = double space.

**Property:** `\Marker`  
**Example:** `\Marker p`  
**Description:** The actual marker (without the backslash).

**Property:** `\Name`  
**Example:** `\Name q1 - Poetry - Indent Level 1`  
**Description:** The name of this marker displayed to the user in the marker selection list. This must be unique for each marker. Edit this to localize the marker names (see: How do I localize the names of USFMs?).

**Property:** `\NotRepeatable`  
**Example:** `\NotRepeatable`  
**Description:** Include if this marker must not be repeated under its parent marker (see: How does the stylesheet specify where a marker is allowed to occur?).

**Property:** `\OccursUnder`  
**Example:** `\OccursUnder c`  
**Description:** A list of markers, separated by spaces, which the current marker may occur under. `\OccursUnder` and `\Rank` work together to specify where a marker is allowed to occur.

If a marker does not have an `\OccursUnder` property, it can occur anywhere in any order. If a marker has an `\OccursUnder` property, then it must have at least one "parent" marker in the OccursUnder list. A "parent" must occur before any occurrence of the marker concerned.

*Example:* Marker `\p` indicates `\OccursUnder c`; this means there must be a preceding chapter marker somewhere before the first `\p`, and it identifies any `\p` paragraphs which occur in the book introduction before the first `\c` as invalid. There may be many `\p` markers occurring after a `\c` marker.

If multiple markers are listed in the `\OccursUnder` property:
* If the marker being described is a paragraph type, at least one of the markers listed must occur before the marker being described.
* If the marker being described is a character type, the list of markers identifies all of the paragraph types within which the marker concerned can occur.

**Property:** `\Rank`  
**Example:** `\Rank 4`  
**Description:** Used with `\OccursUnder` to specify the order of markers when multiple markers occur under the same marker.

If two markers can have the same "parent", specified with `\OccursUnder`, and both have `\Rank` specified, then the rank of the first marker must be less than or equal to the rank of the second marker. For example `\h` has `\Rank 1` and `\OccursUnder id`; marker `\mt1` has `\Rank 3` and `\OccursUnder id`; therefore they both have the same parent and the \h must always come before \mt1.

If `\Rank` is not specified or is specified as 0 then no order is imposed except for the requirements imposed by `\OccursUnder`.

**Property:** `\RightMargin`  
**Example:** `\RightMargin .25`  
**Description:** Amount of right indent given to this paragraph in inches.

**Property:** `\SpaceAfter`  
**Example:** `\SpaceAfter 4`  
**Description:** Amount of extra space after this paragraph measured in points.

**Property:** `\SpaceBefore`  
**Example:** `\SpaceBefore 8`  
**Description:** Amount of extra space before this paragraph measured in points.

**Property:** `\StyleType`  
**Example:** `\StyleType Character`  
**Description:** Must contain one of the following values:
* `Paragraph`: Marker starts beginning of a new paragraph. May contain embedded note or character styles.
* `Character`: Marker applies to a span of characters within a paragraph or note.
* `Note`: Marker starts an embedded note

**Property:** `\Smallcaps`  
**Example:** `\Smallcaps`  
**Description:** Font for this tag is displayed using small caps.

**Property:** `\Superscript`  
**Example:** `\Superscript`  
**Description:** Font for this tag is raised.

**Property:** `\TextProperties`  
**Example:** `\TextProperties paragraph publishable vernacular`  
**Description:** Should contain one of the following values:
* `Verse`: Beginning of new verse. Only present for `\v`.
* `Chapter`: Beginning of the chapter. Only present for `\c`.
* `Paragraph`: Beginning of new paragraph.
* `Publishable`: Text is publishable.
* `Nonpublishable`: Text is not publishable.
* `Vernacular`: Text is in vernacular language.
* `Nonvernacular`: Text is not in vernacular language.
* `Poetic`: Text is poetic.
* `Level_1`, `Level_2`, `Level_3`, `Level_4`, `Level_5`: Level of title, section, or poetic line.
* `CrossReference`: Text contains reference to another portion of Scripture
* `Book`: Beginning of new book. Only present for `\id`.
* `Note`: Beginning of new note.

If a character style marker does not have a “publishable” value (Publishable or Nonpublishable) or a “vernacular” value (Vernacular or Nonvernacular), each occurrence of the character style marker takes the value from the marker of the paragraph which contains it.

**Property:** `\TextType`  
**Example:** `\TextType VerseText`  
**Description:** May only contain one of the following values:
* `Title`: Title for a book.
* `Section`: Section heading.
* `VerseText`: Normal verse body text.
* `NoteText`: Note text, e.g. footnotes and cross references.
* `Other`: Not a Title, Section, VerseText or Note, e.g., introduction, glossary.
* `BackTranslation`: Back translation text.

**Property:** `\Underline`  
**Example:** `\Underline`  
**Description:** Font for this tag is underlined.
