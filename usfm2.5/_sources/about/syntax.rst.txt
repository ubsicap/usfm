.. include:: /_static/inc_styles.txt

.. index:: syntax

Syntax Notes
============

.. contents:: :depth: 2

-----

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

.. _syntax_documentation:
.. index:: syntax (documentation)

Documentation Notes
-------------------
The syntax for individual markers is presented in this manual in a code formatting style. For example:

	``\usfm#(_text...)``
 
* Required spaces are indicated with an underscore ``_``.
* Parameters or variables are indicated in ALLCAPS or by a special character such as the hash mark ``#``. A description of the meaning or use of a variable or parameter is provided below the marker.
* Optional or suggested information is shown as a text example in parentheses – like ``(text...)``. In some cases an underscore in listed within the parentheses, which indicates that the space is needed only when text follows the marker. Most paragraph or poetic markers (like ``\p``, ``\m``, ``\q#`` etc.) can be followed immediately by a verse number (``\v``) on a new line.
