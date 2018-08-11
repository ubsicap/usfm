.. include:: /_static/inc_styles.txt

.. index:: peripherals, marker; \periph, periph

Peripherals
===========

The following strategy should be used for applying USFM markup to project peripheral contents.

Content should be created in separate :doc:`book </identification/books>` files according to the general groupings presented in the table below. As with scripture text books, an :ref:`\\id <usfmp_id>` marker is used for identifying the overall content of the peripheral file. Within each book, divisions (sub-sections) of content are denoted using the marker ``\periph`` followed by an additional division title. Content is added to books and divisions by re-purposing the most appropriate existing USFM marker for the selected content.

Some back matter content is large enough that it is most practical to store it within its own book file (Concordance, Glossary, Topical Index, Names Index). Content self contained within a separate book file does not require an additional identifier (only :ref:`\\id <usfmp_id>`).

.. _periph_div:
.. index:: pair: peripherals; books
	pair: peripherals; divisions

Peripheral Books and Divisions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

+-------------------------------+----------------------------------+------------------------------+
| :doc:`Front Matter <front>`   | :doc:`Introductions <intros>`    | :doc:`Back Matter <back>`    |
| (\\id FRT)                    | (\\id INT)                       | (\\id BAK)                   |
+===============================+==================================+==============================+
| **Divisions**                 | **Divisions**                    | **Divisions**                |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Title Page``        | ``\periph Bible Intorduction``   | ``\periph Chronology Test``  |
| |br| ``|id="title"``          | |br| ``|id="intbible"``          | |br| ``|id="chron"``         |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Half Title Page``   | ``\periph Old Testament          | ``\periph Weights and        |
| |br| ``|id="halftitle"``      | Introduction``                   | Measures``                   |
|                               | |br| ``|id="intot"``             | |br| ``|id="measures"``      |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Promotional Page``  | ``\periph Pentateuch             | ``\periph Map Index``        |
| |br| ``|id="promo"``          | Introduction``                   | |br| ``|id="maps"``          |
|                               | |br| ``|id="intpent"``           |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Imprimatur``        | ``\periph History Introduction`` | ``\periph LXX Quotes in NT`` |
| |br| ``|id="imprimatur"``     | |br| ``|id="inthistory"``        | |br| ``|id="lxxquotes"``     |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Publication Data``  | ``\periph Poetry Introduction``  | **Additional Back Matter**   |
| |br| ``|id="pubdata"``        | |br| ``|id="intpoetry"``         |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Foreword``          | ``\periph Prophecy               | Concordance (\\id CNC)       |
| |br| ``|id="foreword"``       | Introduction``                   |                              |
|                               | |br| ``|id="intprophesy"``       |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Preface``           | ``\periph Deuterocanon           | Glossary (\id GLO)           |
| |br| ``|id="preface"``        | Introduction``                   |                              |
|                               | |br| ``|id="intdc"``             |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Table of Contents`` | ``\periph New Testament          | Topical Index (\id TDX)      |
| |br| ``|id="contents"``       | Introduction``                   |                              |
|                               | |br| ``|id="intnt"``             |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Alphabetical        | ``\periph Gospels Introduction`` | Names Index (\id NDX)        |
| Contents``                    | |br| ``|id="intgospels"``        |                              |
| |br| ``|id="alphacontents"``  |                                  |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Table of            | ``\periph Epistles               | :doc:`Other <other>`         |
| Abbreviations``               | Introduction``                   | **(\\id OTH)**               |
| |br| ``|id="abbreviations"``  | |br| ``|id="intepistles"``       |                              |
+-------------------------------+----------------------------------+------------------------------+
|                               | ``\periph Letters Introduction`` | **Divisions**                |
|                               | |br| ``|id="intletters"``        |                              |
+-------------------------------+----------------------------------+------------------------------+
|                               |                                  | ``\periph Cover``            |
|                               |                                  | |br| ``|id="cover"``         |
+-------------------------------+----------------------------------+------------------------------+
|                               |                                  | ``\periph Spine``            |
|                               |                                  | |br| ``|id="spine"``         |
+-------------------------------+----------------------------------+------------------------------+

.. index:: peripherals; identifiers
.. _periph_id:

Peripheral Identifiers
^^^^^^^^^^^^^^^^^^^^^^

|badge_3.0|

For peripheral books containing :ref:`divisions <periph_div>`, the division title is free-form, and may be expressed in the vernacular language. Whenever possible, a peripheral identifier should be associated with a ``\periph`` division marker. A set of standardized identifiers allow software processes to easily select content for recognized peripheral divisions. The syntax for peripheral identifiers follows the syntax for :doc:`word level attributes </characters/attributes>`: attribute = "value". The attribute name is ``id``. The value is wrapped in quotes.

**Text sample with division identifier attributes:**

.. code-block:: text

	\id FRT
	...
	\periph Title Page|id="title"
	\mt1 Holy Bible
	\mt3 with
	\mt2 Deuterocanonicals/Apocrypha
	...
	\periph Foreword|id="foreword"
	\h Foreword
	\mt1 Foreword
	\p The \bk Good News Translation\bk* of the Bible is a translation which seeks to state 
	clearly and accurately the meaning of the original texts in words and forms that are widely 
	accepted by people who use English as a means of communication.
	...
	\periph Table of Contents|id="contents"
	\h Table of Contents
	\mt Contents
	\s Old Testament
	\tr  \th1 Name  \thr2 Page \th3 Name \thr4 Page
	\tr \tc1 Genesis \tcr2 # \tc3 Ecclesiastes \tcr4 #
	...

Defined peripheral ``id`` values are shown in the peripheral :ref:`divisions <periph_div>` table above.

.. index:: peripherals; user defined divisions
.. _periph_div-user:

User Defined Peripheral Divisions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A project may add peripheral content for a division not defined in the current USFM set. The new division should begin with ``\periph``, plus a division title, and a user defined identifier using the prefix ``x-`` to a user defined ``id`` value. However, USFM compliant publishing applications should consider the defined :ref:`divisions <periph_div>` and identifiers as a reference for content to support.

Markup for Peripheral Divisions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the following topics there is a recommendation and a brief description of the USFM markers which will be most appropriate for use in each peripheral content division. The recommended markup is sufficient for most projects and should be used as a first option. However, in general, any of the existing USFM standard markers may be used in addition to the recommended markers, if the required content cannot be adequately encoded.

.. toctree::
   :maxdepth: 1

   Front Matter <front>
   Introductions <intros>
   Back Matter <back>
   Other <other>

Any non-standard markers used in these books will need to be added to the stylesheet associated with the project.

Authoring peripheral materials within ParaTExt
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
ParaTExt includes the named peripheral :doc:`books </identification/books>` FRT, INT, BAK, CNC, GLO, TDX, NDX, and OTH in addition to a set of books named from XXA to XXG. These non-Biblical books appear at the end of a project's list of books, and may be used to author the non-biblical text for Front Matter, Back Matter, Introductions, or any other kind of text which should be stored as part of the translation project.
