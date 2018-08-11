.. include:: /_static/inc_styles.txt

.. index:: cross references, note (cross reference)

Cross References
================

.. index:: cross reference container

.. rubric:: Cross Reference Container

Cross references are entered inline within the main scripture body text. The boundaries of the cross reference text are defined by an opening and closing marker. The individual elements which make up the cross reference content are described under the heading :ref:`Cross Reference Content Elements <usfmn_x-content>` below.

.. _usfmn_x:
.. index:: marker (\x ...\x*), cross reference (container)

\\x ...\\x\*
------------
:Syntax: ``\x_+_(\xo_REF_)cross reference content\x*``
:Type: note
:Added: 1.0
:Use: Beginning and ending of the cross reference element.

:red:`+`

* The cross reference caller, which may be one of the following three types:

	    :red:`+` – indicates that the caller should be generated automatically by the translation editor, or publishing tools. |br|
	    :red:`-` – indicates that no caller should be generated, and is not used. |br|
	    :red:`?` – where ? represents the character to be used for the caller. The caller is defined for the specific cross reference by the author.

:red:`cross reference content` (see :ref:`below <usfmn_x-content>`)

	* All of the text elements which make up the cross reference:

	    - :ref:`origin <usfmc_xo>` reference
	    - special cross reference elements such as keywords or quotations
	    - :ref:`target <usfmc_xt>` references

	* Each element should be prefixed by the appropriate marker (listed below).

.. note::

	**Important:** See :doc:`Syntax Notes </about/syntax>` for addition information on the use of :ref:`endmarkers <syntax_endmarkerInNotes>` for elements within cross reference content.

.. _usfmn_x-content:
.. index:: cross reference (content)

-----

Cross Reference Content Elements
--------------------------------
The following markup can be included as part of the cross reference content:

.. _usfmc_xo:
.. index:: marker (\xo)

\\xo
^^^^
:Syntax: ``\xo_##SEP##``
:Type: character (note)
:Added: 1.0
:Use: Cross reference origin reference. |br|
	 This is the chapter and verse(s) that :ref:`target reference(s) <usfmc_xt>` are being provided for. |br|
	 ``SEP`` indicates where the appropriate chapter/verse separator should be used (i.e. colon ":", full stop "." etc.)

-----

.. _usfmc_xk:
.. index:: marker (\xk)

\\xk
^^^^
:Syntax: ``\\xk_text...``
:Type: character (note)
:Added: 1.0
:Use: A keyword from the scripture translation text which the :ref:`target reference(s) <usfmc_xt>` also refer to.

-----

.. _usfmc_xq:
.. index:: marker (\xq)

\\xq
^^^^
:Syntax: ``\xq_text...``
:Type: character (note)
:Added: 1.0
:Use: A quotation from the scripture text. |br|
	Use of a quotation would be intended to help the reader to understand the portion of text (or concept) for which the :ref:`target reference(s) <usfmc_xt>` are being supplied. |br|

-----

.. _usfmc_xt:
.. index:: marker (\xt)

\\xt
^^^^
:Syntax: ``\\xt_refs...``
:Type: character (note)
:Added: 1.0
:Use: Target reference(s). |br|
	A list of scripture references, commonly provided as book name abbreviations plus chapter and verse, or range of verses. The punctuation used between chapter and verse, reference ranges, and between target references can differ significantly across texts.

-----

.. _usfmc_xot:
.. index:: marker (\xot ...\xot*)

\\xot ...\\xot\*
^^^^^^^^^^^^^^^^
:Syntax: ``\xot_refs...\xot*``
:Type: character (note)
:Added: 2.2
:Use: References (or other text) between these markers is material to be included only in published editions that contain the Old Testament books. *(optional)*

-----

.. _usfmc_xnt:
.. index:: marker (\xnt ...\xnt*)

\\xnt ...\\xnt\*
^^^^^^^^^^^^^^^^
:Syntax: ``\xnt_refs...\xnt*``
:Type: character (note)
:Added: 2.2
:Use: References (or other text) between these markers is material to be included only in published editions that contain the New Testament books. *(optional)*

-----

.. _usfmc_xdc:
.. index:: marker (\xdc ...\xdc*)

\\xdc ...\\xdc\*
^^^^^^^^^^^^^^^^
:Syntax: ``\xdc_refs...\xdc*``
:Type: character (note)
:Added: 1.0
:Use: References (or other text) between these markers is material to be included only in published editions that contain the Deuterocanonical books. *(optional)*

-----

.. _usfmc_rq-alt:
.. index:: marker (\rq ...\rq*)

\\rq ...\\rq\*
^^^^^^^^^^^^^^
:Syntax: ``\rq ...\rq*``
:Type: character
:Added: 2.05
:Use: Inline quotation reference(s). |br|
	See details and examples in :ref:`Titles, Heading, and Labels <usfmc_rq>`

-----

.. rubric:: Text and Formatting Samples

**Typical Cross Reference** - Matthew 2.23 (GNT)

.. code-block:: text
	:name: usfm-character_xo_xt_example
	:emphasize-lines: 5

	\p
	\v 22 But when Joseph heard that Archelaus had succeeded his father Herod as king of 
	Judea, he was afraid to go there. He was given more instructions in a dream, so he went 
	to the province of Galilee
	\v 23 \x - \xo 2.23: \xt Mrk 1.24; Luk 2.39; Jhn 1.45.\x* and made his home in a town 
	named Nazareth. And so what the prophets had said came true: “He will be called a 
	Nazarene.”

.. image:: images/usfm-character_xo_xt.jpg
	:width: 550px

**Multiple Origin Parts** - Mark 10.19 (GNT)

.. code-block:: text
	:name: usfm-character_xo-multi_example
	:emphasize-lines: 3-4

	\p
	\v 18 “Why do you call me good?” Jesus asked him. “No one is good except God alone.
	\v 19 \x - \xo 10.19: a \xt Exo 20.13; Deu 5.17; \xo b \xt Exo 20.14; Deu 5.18; \xo c 
	\xt Exo 20.15; Deu 5.19; \xo d \xt Exo 20.16; Deu 5.20; \xo e \xt Exo 20.12; Deu 5.16.\x* 
	You know the commandments: ‘Do not commit murder; do not commit adultery; do not steal; 
	do not accuse anyone falsely; do not cheat; respect your father and your mother.’”

.. image:: images/usfm-character_xo-multi.jpg
	:width: 550px

**Deuterocanonical Content** - 1 Corinthians 15.51-52 (GNT)

.. code-block:: text
	:name: usfm-character_xdc_example
	:emphasize-lines: 2

	\p
	\v 51-52 \x - \xo 15.51,52: \xdc 2Es 6.23; \xt 1Th 4.15-17.\x* Listen to this secret 
	truth: we shall not all die, but when the last trumpet sounds, we shall all be changed 
	in an instant, as quickly as the blinking of an eye. For when the trumpet sounds, the 
	dead will be raised, never to die again, and we shall all be changed.

Genesis 1.26 (GNT)

.. code-block:: text
	:name: usfm-character_xdc_example2
	:emphasize-lines: 2

	\p
	\v 26 \x - \xo 1.26: \xt \xdc Wis 2.23; Sir 17.3,4;\xdc* 1Co 11.7.\x* Then God said,
	"And now we will make human beings; they will be like us and resemble us.
