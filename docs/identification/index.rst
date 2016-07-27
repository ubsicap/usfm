.. include:: /_static/inc_styles.txt

.. index:: identification

Identification
==============

.. toctree::
   :maxdepth: 2

   Book Abbreviations <books>

-----

.. _usfmp_id:
.. index:: marker (\id)

\\id
^^^^
:Syntax: ``\id_<CODE>_(Name of file, Book name, Language, Last edited, Date etc.)``
:Type: paragraph
:Added: 1.0
:Use: File identification. |br|
	This is the initial USFM marker in any scripture text file. |br|
	CODE is a standard 3 letter :doc:`scripture book abbreviation <books>`.

**Text and Formatting Sample**

.. code-block:: text
	:name: usfm-paragraph_id_example
	:emphasize-lines: 1

	\id MAT 41MATGNT92.PTX, Good News Translation, June 2003

The text following this marker is not normally used in any formatted presentation.

-----

.. _usfmp_ide:
.. index:: marker (\ide)

\\ide
^^^^^
:Syntax: ``\ide_<ENCODING>``
:Type: paragraph
:Added: 1.0
:Use: An optional character encoding specification. |br|
	This marker should be used to specify the character encoding of the text within the file. For example: CP-1252, CP-1251, UTF-8, UTF-16, OR Custom <specify font name>. If the character encoding does not conform to a known standard, but is rather a customized solution for the project, a minimum of the name of the font used for the project should be included. For archive purposes, texts which rely upon a custom encoding solution should be converted to Unicode, if at all possible. |br|

**Text and Formatting Sample**

.. code-block:: text
	:name: usfm-paragraph_ide_example
	:emphasize-lines: 1-3

	\ide UTF-8
	\ide CP-1252
	\ide Custom (TGUARANI.TTF)

The text following this marker is not normally used in any formatted presentation.

-----

.. _usfmp_sts:
.. index:: marker (\sts)

\\sts
^^^^^
:Syntax: ``\sts_<STATUS CODE>``
:Type: paragraph
:Added: 1.0
:Use: Project text status tracking. |br|
	*The contents of the status marker can be defined by the downstream system* being used to track project status. |br|
	Multiple status entries can be contained in a book to indicate that various portion of the text are present with different draft levels. If an entire book is complete at a given status level, only one status entry is required.

**Text and Formatting Sample**

.. code-block:: text
	:name: usfm-paragraph_sts_example
	:emphasize-lines: 1

	\sts 2

The text following this marker is not normally used in any formatted presentation.

-----

.. _usfmp_rem:
.. index:: marker (\rem)

\\rem
^^^^^
:Syntax: ``\rem_text...``
:Type: paragraph
:Added: 1.0
:Use: Remark. |br|
	For adding brief comments by a translator, consultant, or support person. The text is not a type of footnote and is not intended for publication.

**Text and Formatting Sample**

.. code-block:: text
	:name: usfm-paragraph_rem_example
	:emphasize-lines: 1-2

	\rem Assigned to <translator's name>.
	\rem First draft complete, waiting for checks.

The text following this marker is not normally used in any formatted presentation.

-----

.. _usfmp_h:
.. index:: marker (\h)

\\h
^^^
:Syntax: ``\h_text...``
:Type: paragraph
:Added: 1.0
:Amended: 3.0
:Use: Running header text. |br|
	**Deprecated** use of numbered variable syntax (i.e. use is strongly discouraged). |badge_3.0| |br|
	The variable # in ``\h#_text...`` represented distinct components or levels of text required for the running header presentation (e.g. inside, outside, sub-division/section etc.).

**Text and Formatting Sample** - Matthew (GNT)

.. code-block:: text
	:name: usfm-paragraph_h#_example
	:emphasize-lines: 1

	\h Matthew

.. image:: images/usfm-paragraph_h.jpg
	:width: 250px

-----

.. _usfmp_toc#:
.. index:: marker (\toc#)

\\toc#
^^^^^^
:Syntax: ``\toc1_text...``
:Type: paragraph
:Added: 2.03, 2.04 (\\toc3)
:Use: Long table of contents text. |br| |br|

:Syntax: ``\toc2_text...``
:Use: Short table of contents text. |br| |br|

:Syntax: ``\toc3_text...``
:Use: Book abbreviation. |br|

**Text and Formatting Sample** - Matthew (GNT)

.. code-block:: text
	:name: usfm-paragraph_toc#_example
	:emphasize-lines: 2-4

	\h Matthew
	\toc1 The Gospel According to Matthew
	\toc2 Matthew
	\toc3 Mat

.. image:: images/usfm-paragraph_toc.jpg
	:width: 400px

-----

.. _usfmp_iex:
.. index:: marker (\iex)

\\iex
^^^^^
:Syntax: ``\iex_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction explanatory or bridge text (e.g. explanation of missing book in a short Old Testament). |br|

