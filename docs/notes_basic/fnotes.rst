.. include:: /_static/inc_styles.txt

.. index:: footnotes, note; footnote

Footnotes
=========

.. index:: footnote; container

.. rubric:: Footnote / Endnote Container

Footnotes are entered inline within the main scripture body text. The boundaries of the footnote text are defined by an opening and closing marker. The individual elements which make up the note content are described under the heading :ref:`Footnote Content Elements <usfmn_f-content>` below.

.. _usfmn_f:
.. index:: marker; \f ...\f*

\\f ...\\f\*
------------
:Syntax: ``\f_+_(\fr_REF_)footnote content\f*``
:Type: note
:Added: 1.0
:Use: Beginning and ending of the footnote element.

:red:`+`

* The footnote caller, which may be one of the following three types:

	    :red:`+` – indicates that the caller should be generated automatically by the translation editor, or publishing tools. |br|
	    :red:`-` – indicates that no caller should be generated, and is not used. |br|
	    :red:`?` – where ? represents the character to be used for the caller. The caller is defined for the specific note by the author.			

:red:`footnote content` (see :ref:`below <usfmn_f-content>`)

	* All of the text elements which make up the footnote:

	    - :ref:`origin <usfmc_fr>` reference
	    - special footnote elements such as keywords, quotations, alternate renderings etc.
	    - footnote :ref:`text <usfmc_ft>`

	* Each element should be prefixed by the appropriate marker (listed below).

.. note::

	**Important:** See :doc:`Syntax Notes </about/syntax>` for addition information on the use of :ref:`endmarkers <syntax_endmarkerInNotes>` for elements within footnote content.

.. index:: marker; \fe ...\fe*, footnote; endnote container

.. rubric:: Endnote Syntax

Notes which are intended as "Endnotes" should be marked using the following alternative format:

\\fe ...\\fe\*
--------------
:Syntax: ``\fe_+_(\fr_REF_)endnote content\fe*``
:Type: note
:Added: 1.0
:Use: Beginning and ending of the endnote element.

.. _usfmn_f-content:
.. index:: footnote; content

-----

Footnote Content Elements
-------------------------
The following markup can be included as part of the footnote content:

.. _usfmc_fr:
.. index:: marker; \fr, footnote; origin reference

\\fr
^^^^

:Syntax: ``\fr_##SEP##``
:Type: character (note)
:Added: 1.0
:Use: Footnote origin reference. |br|
	This is the chapter and verse(s) that note refers to. |br|
	``SEP`` indicates where the appropriate chapter/verse separator should be used (i.e. colon ":", full stop "." etc.)

-----

.. _usfmc_fq:
.. index:: marker; \fq, footnote; quotation

\\fq
^^^^

:Syntax: ``\fq_text...``
:Type: character (note)
:Added: 1.0
:Use: Footnote translation quotation. |br|
	A quotation from the current scripture text translation for which the note is being provided. |br|
	Longer quotations are sometimes shortened using an ellipsis (i.e. suspension dots "...").

.. note::

	Many existing translation texts have marked both quotations from the existing translation text, as well as alternative translations, using \fq. An additional marker – :ref:`\\fqa <usfmc_fqa>` – is provided for marking alternative translations, and can be used to distinguish between quotations and alternatives.

**Text and Formatting Samples - Quotations and Alternative Translations** - Mark 1.1; 1.4 (GNT)

.. code-block:: text
	:name: usfm-character_fq_fqa_example
	:emphasize-lines: 4-5

	\s1 The Preaching of John the Baptist
	\r (Matthew 3.1-12; Luke 3.1-18; John 1.19-28)
	\p
	\v 1 This is the Good News about Jesus Christ, the Son of God. \f + \fr 1.1: \ft Some 
	manuscripts do not have \fq the Son of God.\f*
	...

*Footnotes*

.. image:: images/usfm-character_fq.jpg
	:width: 550px

*Footnote caller in body text*

.. image:: images/usfm-character_fq-call.jpg
	:width: 250px

-----

.. _usfmc_fqa:
.. index:: marker; \fqa, footnote; alternate translation

\\fqa
^^^^^

:Syntax: ``\fqa_text...``
:Type: character (note)
:Added: 1.0
:Use: Footnote alternate translation. |br|
	Used to distinguish between a quotation of the current scripture text translation, and an alternate translation.

-----

.. _usfmc_fk:
.. index:: marker; \fk, footnote; keyword

\\fk
^^^^

:Syntax: ``\fk_text...``
:Type: character (note)
:Added: 1.0
:Use: Footnote keyword. |br|
	The specific keyword/term from the text for which the footnote is being provided.

**Text and Formatting Sample** - Genesis 3.20 (GNT)

.. code-block:: text
	:name: usfm-character_fk_example
	:emphasize-lines: 2-4

	\p
	\v 20 Adam \f + \fr 3.20: \fk Adam: \ft This name in Hebrew means “all human beings.”\f* 
	named his wife Eve, \f + \fr 3.20: \fk Eve: \ft This name sounds similar to the Hebrew 
	word for “living,” which is rendered in this context as “human beings.”\f* because she 
	was the mother of all human beings.
	\v 21 And the \nd Lord\nd* God made clothes out of animal skins for Adam and his wife, 
	and he clothed them.

.. image:: images/usfm-character_fk.jpg
	:width: 550px

-----

.. _usfmc_fl:
.. index:: marker; \fl, footnote; label text

\\fl
^^^^

:Syntax: ``\fl_text...``
:Type: character (note)
:Added: 2.03
:Use: Footnote label text. |br|
	Can be used for marking or "labeling" a word or words which are used consistently across certain types of translation notes (such as the words "Or" in an alternative translation note, "Others", "Heb.", "LXX" etc.).

-----

.. _usfmc_fw:
.. index:: marker; \fw, footnote; witness list

\\fw
^^^^

|badge_3.0|

:Syntax: ``\fw_text...``
:Type: character (note)
:Added: 3.0
:Use: Footnote witness list. |br|
	For distinguishing a list of sigla representing witnesses in critical editions.

.. note::

	Apparatus entries of printed critical editions are densely packed with information. One key part is the list of witnesses supporting a specific reading. The witnesses are usually represented by sigla consisting of one character, an abbreviation, or a number. It can be very helpful to distinguish witness lists from other footnote text, which can make it simpler to introduce checking tools for these lists, and to create linking and reader helps in digital representations.

**Text and Formatting Samples** - Matthew 28.14 (Nestle-Aland 29)

.. code-block:: text
	:name: usfm-character_fw_example

	\f ⸀ \fr 28,14 \ft υπο \fw B D 0148. 892\f*

.. image:: images/usfm-character_fw.jpg
	:width: 450px

Matthew 4.1 (Nestle-Aland 29)

.. code-block:: text
	:name: usfm-character_fw_example-alt

	\f ° \fr 4,1 \fw B Δ 700\f*

.. image:: images/usfm-character_fw-alt.jpg
	:width: 450px

-----

.. _usfmc_fp:
.. index:: marker; \fp, footnote; paragraph

\\fp
^^^^

:Syntax: ``\fp_text...``
:Type: character (note)
:Added: 2.03
:Use: Footnote additional paragraph. |br|
	Use this marker to if you need to indicate the start of a new paragraph within a footnote (uncommon).

-----

.. _usfmc_fv:
.. index:: marker; \fv ...\fv*. footnote; verse number

\\fv ...\\fv\*
^^^^^^^^^^^^^^

:Syntax: ``\fv_##\fv*``
:Type: character (note)
:Added: 1.0
:Use: Footnote verse number. |br|
	A verse number in the the text quotation or alternative translation.

.. note::

	This marker will typically be nested within another footnote content element, like :ref:`\\ft <usfmc_ft>`, :ref:`\\fq <usfmc_fq>` or :ref:`\\fqa <usfmc_fqa>`. See :doc:`Nesting Character Markup </characters/nesting>` for details.

**Text and Formatting Sample** - John 7.38 (GNT)

.. code-block:: text
	:name: usfm-character_fv_example
	:emphasize-lines: 7

	\p
	\v 37 On the last and most important day of the festival Jesus stood up and said in a 
	loud voice, “Whoever is thirsty should come to me, and 
	\v 38 whoever believes in me should drink. As the scripture says, ‘Streams of life-
	giving water will pour out from his side.’” \f + \fr 7.38: \ft Jesus' words in verses 
	37-38 may be translated: \fqa “Whoever is thirsty should come to me and drink. 
	\+fv 38\+fv* As the scripture says, ‘Streams of life-giving water will pour out from 
	within anyone who believes in me.’”\f*

.. image:: images/usfm-character_fv.jpg
	:width: 550px

-----

.. _usfmc_ft:
.. index:: marker; \ft, footnote; note text

\\ft
^^^^

:Syntax: ``\ft_text...``
:Type: character (note)
:Added: 1.0
:Use: Footnote text. |br|
	The essential (explanatory) text of the footnote.

-----

.. _usfmc_fdc:
.. index:: marker; \fdc ...\fdc*, footnote; DC only content

\\fdc ...\\fdc\*
^^^^^^^^^^^^^^^^

:Syntax: ``\fdc_text...\fdc*``
:Type: character (note)
:Added: 1.0
:Deprecated: 3.0 |badge_3.0|
:Use: Footnote Deuterocanonical content. |br|
	Text between these markers is material to be included only in published editions that contain the Deuterocanonical books. |br|
	**Deprecated** (use is discouraged). |br| |br|
	|ico_Cg| *Recommended alternate:* General purpose use of :ref:`\\dc ...\\dc\* <usfmc_dc>` or :doc:`nested </characters/nesting>` ``\+dc ...\+dc*`` wherever DC-only content is being marked.

**Text and Formatting Sample** - Hebrews 1.3 (Spanish DHE)

.. code-block:: text
	:name: usfm-character_fdc_example
	:emphasize-lines: 2

	\v 3 Él es el resplandor glorioso de Dios,\f c \fr 1.3: \fk Resplandor: \ft Cf. 
	Jn 1.4-9,14\fdc ; también Sab 7.25-26, donde algo parecido se dice de la sabiduría.\f* 
	la imagen misma de lo que Dios es y el que sostiene todas las cosas con su palabra 
	poderosa. Después de limpiarnos de nuestros pecados, se ha sentado en el cielo, a la 
	derecha del trono de Dios,
	\v 4 y ha llegado a ser superior a los ángeles, pues ha recibido en herencia un título 
	mucho más importante que el de ellos.

-----

.. _usfmc_fm:
.. index:: marker; \fm ...\fm*, footnote; reference mark

\\fm ...\\fm\*
^^^^^^^^^^^^^^

:Syntax: ``\fm_text...\fm*``
:Type: character (note)
:Added: 1.0
:Use: Footnote reference mark. |br|
	Used where two or more locations in the scripture text should ideally refer the reader to the same footnote text (as seen in identical footnote text which is referenced at Gen 2.9 and Gen 2.17 in some translations).

.. warning::

	Because the nature of this marker is related directly to the published form of the text, it is not intended for use in scripture authoring. It may be used during the publishing process to connect two callers to the same footnote text.
