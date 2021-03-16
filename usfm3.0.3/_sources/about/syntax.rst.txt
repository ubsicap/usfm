.. include:: /_static/inc_styles.txt

.. index:: syntax

Syntax Notes
============

.. contents:: :depth: 2
	:local:

-----

.. _syntax_general:
.. index:: syntax; general

General Syntax
--------------

* There are three broad categories of USFM markup - **paragraph**, **character**, and **note** types.
* All USFM markers begin with a backslash character ``\``.
* :doc:`Paragraph </paragraphs/index>` markers end with the next space character.
* :doc:`Character </characters/index>` markers occur in pairs, marking a span of text within a paragraph.
* Note markers also occur in pairs, marking the start and end of the :doc:`footnote </notes_basic/fnotes>`, :doc:`cross reference </notes_basic/xrefs>`, or :doc:`study note </notes_study/index>` content.
* For marker pairs (character and note), the opening marker ends with the next space character (as with paragraph markers). The matching closing marker is identical to the opening marker but ends with an asterisk character ``*``. Example: ``\w grace\w*``.

.. _syntax_numberedMarkers:
.. index:: syntax; numbered markers

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
.. index:: syntax; endmarkers in notes

Endmarkers in Footnotes and Cross References
--------------------------------------------
The boundaries of :doc:`footnote </notes_basic/fnotes>` or :doc:`cross reference </notes_basic/xrefs>` text are defined by an opening and closing marker, as in the following footnote structure example:
 
	``\f_+_(\fr_REF_)footnote content\f*``
 
The individual elements which make up the footnote or cross reference content are defined as character level markers, which means that they each define a beginning and a corresponding end marker. The Paratext translation editor will interpret the presence of a new marker as an implicit closure of any preceding character level marker. For this reason a majority of translation projects over the years have adopted the approach of authoring footnote or cross reference content without supplying the explicit end marker, since it reduces the volume of markup found within the notes. Some examples of the two acceptable markup approaches for notes is provided below (A = implicit closure; B = explicit end marker):
 
A. ``\f + \fk Issac: \ft In Hebrew means "laughter"\f*``
B. ``\f + \fk Issac:\fk* \ft In Hebrew means "laughter"\ft*\f*``

A. ``\f + \fr 1.14 \fq religious festivals; \ft or \fqa seasons.\f*``
B. ``\f + \fr 1.14\fr* \fq religious festivals;\fq* or \fqa seasons.\fqa*\f*``

A. ``\f + \fr 2.4 \fk The \+nd Lord\+nd*: \ft See \+nd Lord\+nd* in Word List.\f*``
B. ``\f + \fr 2.4\fr* \fk The \+nd Lord\+nd*:\fk* \ft See \+nd Lord\+nd* in Word List.\ft*\f*``

.. note:: **Nested** character markers within notes *always* require explicit opening and closing markers, and must use the syntax for :doc:`character marker nesting </characters/nesting>`.


.. _syntax_whitespace:
.. index:: syntax; whitespace, whitespace

Whitespace
----------

USFM considers space (U+0020), tab (U+0009), and :ref:`newline characters <syntax_newline>` to be whitespace.

.. _syntax_whitespace-significant:

* **Significant whitespace** is a critical part of the USFM document and should always be preserved as is.

    - The space after the end of a paragraph marker, or the end of the opening marker within a character or note marker pair.
    - The :ref:`newline <syntax_newline>` preceding a new paragraph marker.

.. _syntax_whitespace-insignificant:

* **Insignificant whitespace** should be :ref:`normalized <syntax_whitespace_normalization>` by a USFM processor.

    - Multiple whitespace within the body text of a :doc:`paragraph </paragraphs/index>`.
    - Multiple whitespace preceding a :doc:`paragraph </paragraphs/index>` marker.

.. _syntax_newline:
.. index:: syntax; newline, newlines

Newlines
^^^^^^^^

USFM processors should treat the single CR (U+000D) or LF  (U+000A) characters, and the sequence Carriage Return-Line Feed (CRLF), like a single LF character. Applications can save documents using the appropriate line-ending convention.

All **paragraph markers** should be preceded by a single newline.

As a *recommended best practice* for USFM editors, **inline markup** (:doc:`character styles </characters/index>`, :doc:`footnotes </notes_basic/fnotes>`, or :doc:`cross references </notes_basic/xrefs>`) should *not* be preceded by a newline. It would be acceptable for a :ref:`whitespace normalization <syntax_whitespace_normalization>` process to replace a newline and any preceding space (multiple spaces) before this inline markup with a single space (#3), but it should not remove all whitespace.

In the following example, the footnote ``\f ...\f*`` at MAT 6:27:

.. code-block:: text

	\v 27 Can any of you live a bit longer
	\f + \fr 6.27: \fq live a bit longer; \ft or \fq grow a bit taller.\f* by worrying about it?

would be normalized as:

.. code-block:: text

	\v 27 Can any of you live a bit longer \f + \fr 6.27: \fq live a bit longer; \ft or \fq grow a 
	bit taller.\f* by worrying about it?

.. _syntax_whitespace_normalization:
.. index:: pair: whitespace; normalization

Whitespace Normalization
^^^^^^^^^^^^^^^^^^^^^^^^

1. Multiple whitespace between the end of a paragraph marker and the paragraph text are normalized to a single space (U+0020).
2. Multiple whitespace between words are normalized to a single space (U+0020).
3. Multiple whitespace between text and a character or note marker (\f\, \ex, \x, \ex; not \esb or \esbe) are normalized to a single space (U+0020).

	* Due to the *extensive common practice* in USFM documents of adding new verse text after a newline, multiple whitespace between text and a verse marker (:ref:`\\v <usfmc_v>`) should be normalized as a single newline.

4. Multiple whitespace preceding a paragraph marker is normalized to a single :ref:`newline <syntax_newline>`.
5. Normalized whitespace preceding and following a character or note marker pair is preserved. (USFM validation tools may flag suspicious whitespace.)
6. Normalized whitespace preceding the closing marker of a character or note marker pair is preserved. (USFM validation tools may flag suspicious whitespace.)
7. :ref:`Significant whitespace <syntax_whitespace-significant>` should not be added to the text.

**Handling special contexts**

The normalization rules outlined in 3,5,7 can result in some whitespace remaining in the text which may be considered insignificant depending on its context.

For example, the space preceding the footnote in:

.. code-block:: text

	\v 27 Can any of you live a bit longer \f + \fr 6.27: \fq live a bit longer;

could be removed:

.. code-block:: text

	\v 27 Can any of you live a bit longer\f + \fr 6.27: \fq live a bit longer;

And a space after a cross reference occurring at the start of a verse

.. code-block:: text

	v 7 \x - \xo 2.7: \xt 1 Co 15.45.\x* Then the \nd Lord\nd* God took some soil 
	from the ground and formed a man

could be removed:

.. code-block:: text

	v 7 \x - \xo 2.7: \xt 1 Co 15.45.\x*Then the \nd Lord\nd* God took some soil 
	from the ground and formed a man

Yet, a normalization process cannot *generally* remove ALL whitespace preceding and following note marker pairs. In many cases a single whitespace is expected between the texts which precede and follows a note. As suggested and recommended earlier:

* USFM validation tools may flag suspicious whitespace
* USFM editors can takes steps to discourage ambiguous whitespace wherever possible
* USFM normalization tools can identify and handles special contexts (examples above)
* USFM publication tools and other post processors can identify and handle special contexts in the manner which is most suitable for the intended output.

.. _syntax_znamespace:
.. index:: marker; \z..., syntax; user namespace

\\z namespace
-------------

If local markup additions/extensions are required, USFM recommends that any additional user generated markup should begin with **\\z** (e.g. ``\zMyMarker``). Markers in this namespace will not be considered a part of the USFM standard, or be generally supported in USFM aware applications. This namespace will acts as a "private use area". It will be the user or tool builder's responsibility to support ``\\z`` markup in ways which meet a local need. Other USFM processing tools cannot be expected to handle ``\\z`` markup or associated text, and are free to ignore them when they are encountered in the text.

.. tip::

	Scripture translation and publishing software `Paratext <http://pt8.paratext.org/>`_ and `Publishing Assistant <http://pubassist.paratext.org/>`_ both provide methods for adding definitions for user generated markers to a specific project's setup. This makes it possible to support proper functioning of checking and formatting tools for the added markup.
 
It is much less likely that digital publishing systems and work-flows will support user-generated/non-standardized project markup automatically. Current procedures for interacting with these partner environments requires that translation data is delivered in well-defined and validated formats, which conform to agreed specifications, such as the USFM marker inventory, or some XML-based equivalents. Since these digital workflows are much more exclusively software-driven than area many print production tools, encountering unknown markup within the publishing processes is a major problem. Please consider this carefully before introducing non-standard USFM markup within a scripture translation project text.

.. _syntax_documentation:
.. index:: syntax; documentation

Documentation Syntax Notes
--------------------------
The syntax for individual markers is presented in this manual in a code formatting style. For example:

	``\usfm#(_text...)``
 
* Required spaces are indicated with an underscore ``_``.
* Parameters or variables are indicated in ALLCAPS or by a special character such as the hash mark ``#``. A description of the meaning or use of a variable or parameter is provided below the marker.
* Optional or suggested information is shown as a text example in parentheses – like ``(text...)``. In some cases an underscore in listed within the parentheses, which indicates that the space is needed only when text follows the marker. Most paragraph or poetic markers (like ``\p``, ``\m``, ``\q#`` etc.) can be followed immediately by a verse number (``\v``) on a new line.
