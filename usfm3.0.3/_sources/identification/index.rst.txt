.. include:: /_static/inc_styles.txt

.. index:: identification

Identification
==============

.. toctree::
   :maxdepth: 2

   Book Abbreviations <books>

-----

.. _usfmp_id:
.. index:: marker; \id, identification; file

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

	\id MAT 41MATGNT92.SFM, Good News Translation, June 2003

The text following this marker is not normally used in any formatted presentation.

-----

.. _usfmp_usfm:
.. index:: marker; \usfm, identification; usfm version id

\\usfm
^^^^^^

|badge_3.0|

:Syntax: ``\usfm_<USFM version number>``
:Type: paragraph
:Added: 3.0
:Use: USFM version specification for the file. |br|
	Used to identify the USFM version which a USFM editor / processor will be required to support in order to manage all markup found within the file.

**Text Sample**

.. code-block:: text
	:name: usfm-paragraph_usfm_example
	:emphasize-lines: 2

	\id MAT 41MATGNT92.SFM, Good News Translation, June 2003
	\usfm 3.0

-----

.. _usfmp_ide:
.. index:: marker; \ide, identification; character encoding, encoding

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
.. index:: marker; \sts, identification; text status

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
.. index:: marker; \rem, identification; remark/comment

\\rem
^^^^^

:Syntax: ``\rem_text...``
:Type: paragraph
:Added: 1.0
:Use: Remark. |br|
	For adding brief comments by a translator, consultant, or support person. The text is not a type of footnote and is not intended for publication. When `\rem` is used, it is often found at the top of a USFM file together with other identification material. However, the use of `\rem` is not limited to this section of a USFM file. It can be used for adding a paragraph containing non-publishable remarks / comments anywhere within a text.

**Text and Formatting Sample**

.. code-block:: text
	:name: usfm-paragraph_rem_example
	:emphasize-lines: 1

	\rem First draft complete, waiting for checks.

The text following this marker is not normally used in any formatted presentation.

.. warning::

	Adding names of individuals, initials, or other personal information directly within scripture text files is *strongly discouraged*.

-----

.. _usfmp_h:
.. index:: marker; \h, identification; header text

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
.. index:: marker; \toc#, identification; contents texts

\\toc#
^^^^^^

:Syntax: ``\toc1_text...``
:Type: paragraph
:Added: 2.03, 2.04 (\\toc3)
:Use: Long table of contents text. |br| |br|

:Syntax: ``\toc2_text...``
:Use: Short table of contents text. |br| |br|

:Syntax: ``\toc3_text...``
:Use: Book abbreviation. Commonly used for books names in a list of cross-reference :ref:`target references <usfmc_xt>`. |br|

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

Matthew (Spanish DHH)

.. code-block:: text
	:name: usfm-paragraph_toc#_example-alt
	:emphasize-lines: 2-4
	
	\h San Mateo
	\toc1 Evangelio según San Mateo
	\toc2 San Mateo
	\toc3 Mt 

-----

.. _usfmp_toca#:
.. index:: marker; \toca#, identification; alternative language contents texts

\\toca#
^^^^^^^

|badge_3.0|

:Syntax: ``\toca1_text...``
:Type: paragraph
:Added: 3.0
:Use: Alternative language long table of contents text. |br|
	Used to specify an alternate set of table of contents texts (for example, in a language of wider communication). |br| |br|

:Syntax: ``\toca2_text...``
:Use: Alternative language short table of contents text. |br| |br|

:Syntax: ``\toca3_text...``
:Use: Alternative language book abbreviation.
