.. include:: /_static/inc_styles.txt

.. index:: syntax

Syntax Notes
============

.. contents:: :depth: 2
	:local:

-----

.. _syntax_general:
.. index:: syntax (general)

General Syntax
--------------

* There are three broad categories of USFM markup - **paragraph**, **character**, and **note** types.
* All USFM markers begin with a backslash character ``\``.
* :doc:`Paragraph </paragraphs/index>` markers end with the next space character.
* :doc:`Character </paragraphs/index>` markers occur in pairs, marking a span of text within a paragraph.
* Note markers also occur in pairs, marking the start and end of the :doc:`footnote </notes_basic/fnotes>`, :doc:`cross reference </notes_basic/xrefs>`, or :doc:`study note </notes_study/index>` content.
* For marker pairs (character and note), the opening marker ends with the next space character (as with paragraph markers). The matching closing marker is identical to the opening marker but ends with an asterisk character ``*``. Example: ``\w grace\w*``.

.. _syntax_numberedMarkers:
.. index:: syntax (numbered markers)

Numbered Markers
----------------
Some USFM markers include an optional numeric variable, which is represented in this documentation by a hash character ``#``. In USFM the number indicates:

* A portion of a complete element, or relative weighting of the "pieces" of the elements, such as ``\mt1``, ``\mt2``, ``\mt3`` which are all parts of a major title.
* The level of division (hierarchy).
* The level of indentation relative to other like elements, as in poetry (``\q#``) or lists (``\li#``) or outlines (``\io#``).

**\marker = \marker1** — The unnumbered version may be used when only one level of \marker exists within the project text. Numbers should always be included when more than one level of the marker exists within the project text.
 
.. warning::

	The variable # should not be used to indicate a specific occurrence in scripture of the element type (e.g. using \\s3 to represent the location of the particular section heading before the "Story of Creation" in Genesis 1.)

.. _syntax_endmarkerInNotes:
.. index:: syntax (endmarkers in notes)

Endmarkers in Footnotes and Cross References
--------------------------------------------
The boundaries of :doc:`footnote </notes_basic/fnotes>` or :doc:`cross reference </notes_basic/xrefs>` text are defined by an opening and closing marker, as in the following footnote structure example:
 
	``\f_+_(\fr_REF_)footnote content\f*``
 
The individual elements which make up the footnote or cross reference content are defined as character level markers, which means that they each define a beginning and a corresponding end marker. The Paratext translation editor will interpret the presence of a new marker as an implicit closure of any preceding character level marker. For this reason a majority of translation projects have adopted the approach of authoring footnote or cross reference content without supplying the explicit end marker. Some examples of the two acceptable markup approaches for notes is provided below (A = implicit closure; B = explicit end marker):
 
A. ``\f + \fk Issac:\ft In Hebrew means "laughter"\f*``
B. ``\f + \fk Issac:\fk* In Hebrew means "laughter"\f*``

A. ``\f + \fr 1.14 \fq religious festivals;\ft or \fq seasons.\f*``
B. ``\f + \fr 1.14\fr* \fq religious festivals;\fq* or \fq seasons.\fq*\f*``

A. ``\f + \fr 2.4 \fk The \nd Lord\nd*: \ft See \nd Lord\nd* in Word List.\f*``
B. ``\f + \fr 2.4\fr* \fk The \nd Lord\nd*:\fk* See \nd Lord\nd* in Word List.\f*``

.. _syntax_whitespace:
.. index:: syntax (whitespace)

Whitespace
----------

USFM considers space (U+0020), tab (U+0009), and :ref:`newline characters <syntax_newline>` to be whitespace.

* **Significant whitespace** is a critical part of the USFM document and should always be preserved as is.

    - The space after the end of a paragraph marker, or the end of the opening marker within a character or note marker pair.
    - The :ref:`newline <syntax_newline>` preceding a new paragraph marker.

* **Insignificant whitespace** should be :ref:`normalized <syntax_whitespace_normalization>` by a USFM processor.

    - Multiple whitespace within the body text of a :doc:`paragraph </paragraphs/index>`.
    - Multiple whitespace preceding a :doc:`paragraph </paragraphs/index>` marker.

.. _syntax_newline:
.. index:: syntax (newline)

Newlines
^^^^^^^^

USFM processors should treat the single CR (U+000D) or LF  (U+000A) characters, and the sequence Carriage Return-Line Feed (CRLF), like a single LF character. Applications can save documents using the appropriate line-ending convention.

All paragraph markers should be preceded by a single newline.

.. _syntax_whitespace_normalization:
.. index:: syntax (whitespace)

Whitespace Normalization
^^^^^^^^^^^^^^^^^^^^^^^^

* Multiple spaces between the end of a paragraph marker and the paragraph text are normalized to a single space.
* Multiple spaces between words are normalized to a single space character.
* Multiple spaces between text and a character marker are normalized to a single space.
* Multiple whitespace preceding a paragraph marker is normalized to a single :ref:`newline <syntax_newline>`.
* Normalized whitespace preceding and following a character or note marker pair is preserved. (USFM validation tools may flag suspicious whitespace.)
* Normalized whitespace preceding the closing marker of a character or note marker pair is preserved. (USFM validation tools may flag suspicious whitespace.)

.. _syntax_znamespace:
.. index:: marker (\z ...)

\\z namespace
-------------

As a means of offering a type of solution to the need for occasional local markup additions/extension, USFM recommends that any additional user generated markup should begin with **\\z** (e.g. ``\zMyMarker``). Markers in this namespace will not be considered a part of the USFM standard, or be generally supported in USFM aware applications. This namespace will acts as a type of "private use area". It will be the user or tool builder's responsibility to support support \\z markup in ways which meet a local need. Other USFM processing tools cannot be expected to handle \\z markup or associated text, and are free to ignore them when they are encountered in the text.

.. tip::

	Scripture translation and publishing software `ParaTExt <http://paratext.org/about/pt>`_ and `Publishing Assistant <http://paratext.org/about/pa>`_ both provide a mechanism for adding information about user generated or customized markers to a specific project's configuration. This makes it possible to support proper functioning of checking and formatting tools for the added markup.
 
However, it is much less likely that emerging digital publishing systems and work-flows will support user-generated/non-standardized project markup. Current procedures for interacting with these partner environments requires that translation data is delivered in rigidly validated formats which conform to specific agreed-upon interchange standards, such as the known USFM marker inventory, or some XML-based equivalents. Since connecting with these environments is much more exclusively software-driven than with many print production tools, encountering unknown markup within the publishing processes is a significant problem. Please consider this carefully before introducing non-standard USFM markup within a scripture translation project text.

.. _syntax_documentation:
.. index:: syntax (documentation)

Documentation Syntax Notes
--------------------------
The syntax for individual markers is presented in this manual in a code formatting style. For example:

	``\usfm#(_text...)``
 
* Required spaces are indicated with an underscore ``_``.
* Parameters or variables are indicated in ALLCAPS or by a special character such as the hash mark ``#``. A description of the meaning or use of a variable or parameter is provided below the marker.
* Optional or suggested information is shown as a text example in parentheses – like ``(text...)``. In some cases an underscore in listed within the parentheses, which indicates that the space is needed only when text follows the marker. Most paragraph or poetic markers (like ``\p``, ``\m``, ``\q#`` etc.) can be followed immediately by a verse number (``\v``) on a new line.
