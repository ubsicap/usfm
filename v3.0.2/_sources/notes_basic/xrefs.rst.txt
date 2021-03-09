.. include:: /_static/inc_styles.txt

.. index:: cross references, note; cross reference

Cross References
================

.. index:: cross reference; container

.. rubric:: Cross Reference Container

Cross references are entered inline within the main scripture body text. The boundaries of the cross reference text are defined by an opening and closing marker. The individual elements which make up the cross reference content are described under the heading :ref:`Cross Reference Content Elements <usfmn_x-content>` below.

.. _usfmn_x:
.. index:: marker; \x ...\x*

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
.. index:: cross reference; content

-----

Cross Reference Content Elements
--------------------------------
The following markup can be included as part of the cross reference content:

.. _usfmc_xo:
.. index:: marker; \xo, cross reference; origin reference

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
.. index:: marker; \xk, cross reference; keyword

\\xk
^^^^

:Syntax: ``\\xk_text...``
:Type: character (note)
:Added: 1.0
:Use: A keyword from the scripture translation text which the :ref:`target reference(s) <usfmc_xt>` also refer to.

-----

.. _usfmc_xq:
.. index:: marker; \xq, cross reference; quotation

\\xq
^^^^

:Syntax: ``\xq_text...``
:Type: character (note)
:Added: 1.0
:Use: A quotation from the scripture text. |br|
	Use of a quotation would be intended to help the reader to understand the portion of text (or concept) for which the :ref:`target reference(s) <usfmc_xt>` are being supplied. |br|

-----

.. _usfmc_xt:
.. index:: marker; \xt, cross reference; target reference(s)

\\xt
^^^^

:Syntax: ``\\xt_refs...``
:Type: character (note)
:Added: 1.0
:Updated: 3.0 (attributes)
:Use: Target reference(s). |br|
	A list of scripture references, commonly provided as book name abbreviations plus chapter and verse, or range of verses. The punctuation used between chapter and verse, reference ranges, and between target references can differ significantly across texts.

**Text and Formatting Samples - Typical Cross Reference** - Matthew 2.23 (GNT)

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

.. _usfmc_xt-attr:
.. index:: attributes; \xt ...\xt*, cross reference; target reference(s) attributes

.. rubric:: Attributes |ico_Tag|

|badge_3.0|

Following the syntax for :doc:`word level attributes </attributes/index>` and the definitions for :doc:`linking attributes </linking/index>`, ``\xt ...\xt`` provides the linking attribute :ref:`link-href <usfmc-attr_link-href>` as a :ref:`default attribute <attributes_default>`.

.. index:: marker; \xt ...|link-href\xt*

:link-href: Unambiguously identifies the scripture target reference using a standard scripture reference format. *(default)* |br|
	Book names must be one a standard :doc:`book identifier </identification/books>`. Chapter verse separator is always a colon ``:``. A string of pattern ``[A-Z1-4]{3}(-[A-Z1-4]{3})? ?[a-z0-9\-:]*`` |br| |br|
	In some scenarios a target reference is written in a format which cannot be accurately parsed and identified. Providing the ``link-href`` attribute allows greater flexibility in the use of ``\xt ...\xt*``. |br| |br| 
	In this context, ``link-href`` should only target scripture references for the current text (i.e. references to other project texts or non-scripture URIs are not allowed) |br| |br|
	When adding ``link-href``, the explicit attribute name is not required since it is defined in USFM as the :ref:`default <attributes_default>` for ``\xt ...\xt*``.

**Text Sample** - Genesis 2 (Russian Synodal, Protestant Version, extending the sample for :ref:`\\cd <usfmp_cd>` - chapter description)

.. code-block:: text
	:name: usfm-paragraph_cd-xt_example
	:emphasize-lines: 2-3

	\c 2
	\cd \xt 1|GEN 2:1\xt* Бог благословляет седьмой день; \xt 8|GEN 2:8\xt* человек в раю Едемском; 
	четыре реки; дерево познания добра и зла. \xt 18|GEN 2:18\xt* Человек дает названия животным. 
	\xt 21|GEN 2:21\xt* Создание женщины.
	\p
	\v 1 Так совершены небо и земля и все воинство их.
	\p
	\v 2 И совершил Бог к седьмому дню дела Свои, которые Он делал, и почил в день седьмой 
	от всех дел Своих, которые делал.

A number (7) alone marked with ``\xt ...\xt*`` is ambiguous, since it could refer to chapter 7 or verse 7 (in `Paratext <https://paratext.org>`_, a number alone is interpreted as a chapter reference). Extending ``\xt ...\xt*`` with the ``link-ref`` attribute makes it possible to express the target reference unambiguously.

.. code-block:: text
	:name: usfm-paragraph_cd_example-alt

	\xt 7|MAT 6:7\xt*
	\xt verse 7|MAT 6:7\xt*
	\xt v7|MAT 6:7\xt*

-----

.. _usfmc_xta:
.. index:: marker; \xta, cross reference; extra/added text

\\xta
^^^^^

|badge_3.0|

:Syntax: ``\\xta_text...``
:Type: character (note)
:Added: 3.0
:Use: Target reference(s) extra / added text. |br|
	Used for marking text which should be ignored when identifying or linking to cross reference target references.

**Text and Formatting Sample** - Matthew 3.0 (GNT - *text and markup adapted*)

.. code-block:: text
	:name: usfm-character_xta_example
	:emphasize-lines: 2-3

	\c 3
	\s1 The Preaching of John the Baptist\x - \xo 3.0 \xta Compare with \xt Mk 1.1-8; 
	Lk 3.1-18; \xta and \xt Jn 1.19-28 \xta parallel passages.\x*
	\p
	\v 1 At that time John the Baptist came to the desert of Judea and started preaching.

.. image:: images/usfm-character_xop_xta.jpg
	:width: 550px

-----

.. _usfmc_xop:
.. index:: marker; \xop ...\xop*, cross reference; published origin reference

\\xop ...\\xop\*
^^^^^^^^^^^^^^^^

|badge_3.0|

:Syntax: ``\xop_text...\xop*``
:Type: character (note)
:Added: 3.0
:Use: Published cross reference origin text. |br|
	In some texts, the content intended to be published in the position of the cross reference origin text ``\xo`` does not follow the typical ``<chapter><separator><verse>`` pattern. An origin reference following this pattern is required for validation of the cross reference location. ``\xop ...\xop*`` can be used in order to supply the content intended for publishing, similar to the use of :ref:`\\cp <usfmp_cp>` and :ref:`\vp ...\vp* <usfmc_vp>`.

**Text and Formatting Sample** - Jonah 1.1-5 (Bulgarian Orthodox Bible)

.. code-block:: text
	:name: usfm-character_xop_example
	:emphasize-lines: 2,4,9,11

	\p
	\v 1 \x - \xo 1:1 \xop Гл 1. (1)\xop* \xt 4 Царств. 14:25.\x*И биде слово Господне 
	към Иона, син Аматиев:
	\v 2 \x - \xo 1:2 \xop (2)\xop* \xt Бит. 10:11. Иона 3:3.\x*„стани, иди в Ниневия, 
	град голям, и проповядвай в него, защото злодеянията му достигнаха до Мене“.
	\v 3 И стана Иона да побегне в Тарсис от лицето Господне; дойде в Иопия и намери кораб, 
	който отиваше за Тарсис, плати за превоз и влезе в него, за да отплува с тях в Тарсис 
	от лицето Господне.
	\v 4 \x - \xo 1:4 \xop (4)\xop* \xt Пс. 106:25.\x*Но Господ подигна в морето силен 
	вятър, и стана в морето голяма буря, и корабът насмалко оставаше да се разбие.
	\v 5 \x - \xo 1:5 \xop (5)\xop* \xt 4 Царств. 17:29.\x*Уплашиха се корабниците; те 
	викаха всеки към своя бог и почнаха да хвърлят в морето товара от кораба, за да му 
	олекне от него; а Иона бе слязъл в дъното на кораба, бе легнал и дълбоко заспал.

.. image:: images/usfm-character_xop.jpg
	:width: 550px

-----

.. _usfmc_xot:
.. index:: marker; \xot ...\xot*, cross reference; OT only content

\\xot ...\\xot\*
^^^^^^^^^^^^^^^^

:Syntax: ``\xot_refs...\xot*``
:Type: character (note)
:Added: 2.2
:Use: References (or other text) between these markers is material to be included only in published editions that contain the Old Testament books. *(optional)*

-----

.. _usfmc_xnt:
.. index:: marker; \xnt ...\xnt*, cross reference; NT only content

\\xnt ...\\xnt\*
^^^^^^^^^^^^^^^^

:Syntax: ``\xnt_refs...\xnt*``
:Type: character (note)
:Added: 2.2
:Use: References (or other text) between these markers is material to be included only in published editions that contain the New Testament books. *(optional)*

-----

.. _usfmc_xdc:
.. index:: marker; \xdc ...\xdc*, cross reference; DC only content

\\xdc ...\\xdc\*
^^^^^^^^^^^^^^^^

:Syntax: ``\xdc_refs...\xdc*``
:Type: character (note)
:Added: 1.0
:Deprecated: 3.0 |badge_3.0|
:Use: References (or other text) between these markers is material to be included only in published editions that contain the Deuterocanonical books.|br|
	**Deprecated** (use is discouraged). |br| |br|
	|ico_Cg| *Recommended alternate:* General purpose use of :ref:`\\dc ...\\dc\* <usfmc_dc>` or :doc:`nested </characters/nesting>` ``\+dc ...\+dc*`` wherever DC-only content is being marked.

**Text and Formatting Samples** - Psalm 115.3-4 (GNT - cross references)

.. code-block:: text
	:name: usfm-character_xdc_example
	:emphasize-lines: 5

	\q1
	\v 3 Our God is in heaven;
	\q2 he does whatever he wishes.
	\q1
	\v 4 \x - \xo 115.4-8: \xt Ps 135.15-18; \xdc Ltj Jr 4-73; \xt Rev 9.20.\x* Their 
	gods are made of silver and gold,
	\q2 formed by human hands.

1 Corinthians 15.51-52 (GNT - cross reference)

.. code-block:: text
	:name: usfm-character_xdc_example2
	:emphasize-lines: 2

	\p
	\v 51-52 \x - \xo 15.51,52: \xdc 2Es 6.23; \xt 1Th 4.15-17.\x* Listen to this secret 
	truth: we shall not all die, but when the last trumpet sounds, we shall all be changed 
	in an instant, as quickly as the blinking of an eye. For when the trumpet sounds, the 
	dead will be raised, never to die again, and we shall all be changed.

-----

.. _usfmc_rq-alt:
.. index:: marker; \rq ...\rq*, cross reference; inline quotation reference(s)

\\rq ...\\rq\*
^^^^^^^^^^^^^^

:Syntax: ``\rq ...\rq*``
:Type: character
:Added: 2.05
:Use: Inline quotation reference(s). |br|
	See details and examples in :ref:`Titles, Heading, and Labels <usfmc_rq>`