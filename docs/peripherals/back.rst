.. include:: /_static/inc_styles.txt

.. index:: peripherals; back matter, back matter, book; \id BAK

.. _usfm-book_BAK:

Back Matter
===========

The BAK :doc:`book </identification/books>` and its :ref:`divisions <periph_div>` can be used for storing material which is typically presented at the end of a scripture publication. In practice some back matter content is large enough to require storing it in its own book file (:ref:`Concordance <usfm-book_CNC>`, :ref:`Glossary <usfm-book_GLO>`, :ref:`Topical Index <usfm-book_CNC>`, :ref:`Names Index <usfm-book_NDX>`).

**General**

Use the following markup (or other appropriate USFM, as required) to create general back matter information or introductory content.

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\p <usfmp_p>` - Paragraph.
* :ref:`\\m <usfmp_m>` - Flush left (margin) paragraph.
* :ref:`\\pi# <usfmp_pi#>` - Indented paragraph.
* :ref:`\\li# <usfmp_li#>` - List item.
* :ref:`\\q# <usfmp_q#>` - Poetic line.

.. index:: periph; Chronology, chronology

\\periph Chronology
^^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\is# <usfmp_is#>` - Introduction heading.
* :ref:`\\ip <usfmp_ip>` - Introduction paragraph.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.

.. index:: periph; Weights and Measures, weights and measures

\\periph Weights and Measures
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\is# <usfmp_is#>` - Introduction heading.
* :ref:`\\ip <usfmp_ip>` - Introduction paragraph.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.

.. index:: periph; Map Index, map index

\\periph Map Index
^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\is# <usfmp_is#>` - Introduction heading.
* :ref:`\\ip <usfmp_ip>` - Introduction paragraph.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.
* :ref:`\\xt ...\\xt\* <usfmc_xt>` - Index target references.

**Text Sample**

In the following example, the variable # represents the location of a page number, to be inserted during the typesetting process.

.. code-block:: text
	:name: periph-mapIndex_example
	:emphasize-lines: 3

	\id BAK
	...
	\periph Map Index
	\mt1 Map Index
	\ip This atlas contains the following maps. Since a number of these maps are especially 
	helpful when reading specific books of the Bible, some have also been placed within the 
	text of the Bible. The page number indicated below will help you find these maps both 
	within the text and within this atlas.
	\tr \th1 Map \thr2 Page
	\tr \tc1 Ancient World \tcr2 #
	\tr \tc1 Egypt and Sinai \tcr2 # 
	\tr \tc1 Division of Canaan \tcr2 # 
	\tr \tc1 United Israelite Kingdom \tcr2 # 
	\tr \tc1 The Assyrian Empire \tcr2 #
	\tr \tc1 Jerusalem in Old Testament Times \tcr2 #
	\tr \tc1 The Kingdoms of Israel and Judah \tcr2 # 
	\tr \tc1 Palestine in the Time of the Maccabees \tcr2 # 
	\tr \tc1 Palestine in the Time of Jesus \tcr2 #
	\tr \tc1 Palestine and Syria \tcr2 #
	\tr \tc1 Paul's First and Second Journeys \tcr2 #
	\tr \tc1 Paul's Third Journey \tcr2 # 
	\tr \tc1 Paul's Journey to Rome \tcr2 # 
	\tr \tc1 Jerusalem in New Testament Times \tcr2 # 
	\tr \tc1 The World of the New Testament \tcr2 #
	\s1 Index to Places
	\s2 A
	\tr \th1 Place \tc2 Map \tcr3 Page
	\tr \tc1 Abel \tc2 United Israelite Kingdom \tcr3 #
	\tr \tc1 Abila \tc2 Palestine in the Time of Jesus\tcr3 #
	\tr \tc1 Abilene \tc2 Palestine in the Time of Jesus\tcr3 #
	\tr \tc1 Accad \tc2 Ancient World\tcr3 #
	...
	\s2 B
	\tr \tc1 Baal Zephon \tc2 Egypt and Sinai \tcr3 # 
	\tr \tc1 Babylon \tc2 The Assyrian Empire \tcr3 # 
	\tr \tc1 Babylonia \tc2 The Assyrian Empire \tcr3 #
	...

.. index:: periph; NT Quotes from LXX, NT quotes from LXX

\\periph NT Quotes from LXX
^^^^^^^^^^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\ip <usfmp_ip>` - Introduction paragraph.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\p <usfmp_p>` - Paragraph.
* :ref:`\\k ...\\k\* <usfmc_k>` - Keyword.

**Text Sample**

.. code-block:: text
	:name: periph-ntQuotesLxx_example
	:emphasize-lines: 3

	\id BAK
	...
	\periph NT Quotes from LXX 
	\ip The writers of the New Testament generally quoted or paraphrased the ancient Greek 
	translation of the Old Testament, commonly known as the Septuagint Version (LXX), made 
	some two hundred years before the time of Christ.
	... 
	\p \k Matthew 1.23\k* (Isaiah 7.14) A virgin will become pregnant and have a son. 
	\p \k Matthew 3.3\k* (Isaiah 40.3) Someone is shouting in the desert, “Prepare a road 
	for the Lord; make a straight path for our God to travel!” 
	\p \k Matthew 12.21\k* (Isaiah 42.4) And on him all people will put their hope.
	...

-----

The following back matter content should each be created within their own book file.

.. _usfm-book_CNC:
.. index:: concordance, book; \id CNC

Concordance
^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\is# <usfmp_is#>` - Introduction heading.
* :ref:`\\ip <usfmp_ip>` - Introduction paragraph.
* :ref:`\\s# <usfmp_s#>` - Section heading (e.g. headings of alphabetical divisions - "A", "B", "C" etc.)
* :ref:`\\p <usfmp_p>` - Main entry + example "cut string" *(required)*.
* :ref:`\\k ...\\k\* <usfmc_k>` - Main entry keyword *(required)*.
* :ref:`\\d <usfmp_d>` - Keyword description.
* :ref:`\\xt ...\\xt\* <usfmc_xt>` - Entry target reference(s) *(required)*.
* :ref:`\\bd ...\\bd\* <usfmc_bd>` - Highlight of the main entry within the cut string (bold).
* :ref:`\\pi <usfmp_pi#>` - Sub-entries, or secondary paragraph(s) (if indentation is preferred).
* :ref:`\\add ...\\add\* <usfmc_add>` - Grammar abbreviation (optional).
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.
* \\xtSee ...\\xtSee\* - Alternate entry target reference. (= custom Concordance and Names Index markup).
* \\xtSeeAlso ...\\xtSeeAlso\* - Additional entry target reference. (= custom Concordance and Names Index markup).

**Text Sample**

.. code-block:: text
	:name: periph-concordance_example
	:emphasize-lines: 1

	\id CNC
	\mt Concordance
	\ip The entries in this concordance have been carefully selected by a team of editors. 
	They have aimed to include all of the verses most likely to be looked up.
	\ip A concordance of this size cannot include every occurrence of each individual word.
	...
	\s A
	\p \k Abandon\k*
	\p \xt Lev 19.4\xt* Do not \bd abandon\bd* me and worship idols.
	\p \xt Deu 31.6\xt* He will not fail you or \bd abandon\bd* you.”
	\p \xt Deu 32.15\xt* They \bd abandoned\bd* God their Creator
	...
	\p \k Able\k*
	\p \xt Exo 31.3\xt* understanding, skill, and \bd ability\bd*
	\p \xt Dan 3.17\xt* If the God whom we serve is \bd able\bd*
	\p \xt Mat 26.61\xt* and said, “This man said, ‘I am \bd able\bd*
	...
	\s B

.. _usfm-book_GLO:
.. index:: glossary, book; \id GLO

Glossary
^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\is# <usfmp_is#>` - Introduction heading.
* :ref:`\\ip <usfmp_ip>` - Introduction paragraph.
* :ref:`\\s# <usfmp_s#>` - Section heading (e.g. headings of alphabetical divisions - "A", "B", C" etc.)
* :ref:`\\p <usfmp_p>` - Main entry *(required)*. May also be used for any additional paragraphs in the definition entry (optional).
* :ref:`\\k ...\\k\* <usfmc_k>` - Main entry keyword *(required)*.
* :ref:`\\pi <usfmp_pi#>` - Sub-entries, or secondary paragraph(s) (if indentation is preferred).
* :ref:`\\li# <usfmp_li#>` - List item.
* :ref:`\\tl ...\\tl\* <usfmc_tl>` - National idiom word(s).

**Text Sample**

.. code-block:: text
	:name: periph-glossary_example
	:emphasize-lines: 1

	\id GLO
	\mt Glossary
	\ip This dictionary is divided into 21 sections. The indexes below list all of the 
	sections, and all of the entries in alphabetical order, so that you can find what you 
	are looking for more easily.
	\p \k Angel\k* A supernatural being who tells God's messages to people or protects those 
	who belong to God.
	...
	\p \k Council\k* (1) A group of leaders who meet and make decisions for their people.
	\pi (2) The Old Testament refers to God's council as a group of angels who meet and talk 
	with God in heaven.
	...

.. _usfm-book_TDX:
.. index:: topical index, book; \id TDX

Topical Index
^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\is# <usfmp_is#>` - Introduction heading.
* :ref:`\\ip <usfmp_ip>` - Introduction paragraph.
* :ref:`\\s# <usfmp_s#>` - Section heading (e.g. headings of alphabetical divisions - "A", "B", "C" etc.)
* :ref:`\\p <usfmp_p>` - Main entry + example "cut string" *(required)*.
* :ref:`\\k ...\\k\* <usfmc_k>` - Main entry keyword *(required)*.
* :ref:`\\xt ...\\xt\* <usfmc_xt>` -  Entry target reference(s) *(required)*. More than one \\xt ...\\xt\* entry can be provided to create logical groupings of references (per chapter; per book etc.).
* :ref:`\\pi <usfmp_pi#>` - Sub-entries, or secondary paragraph(s) (if indentation is preferred).
* :ref:`\\li# <usfmp_li#>` - List item. Use for simple lists, where more complex tabular layout is not required.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.

**Text Sample**

.. code-block:: text
	:name: periph-topicalIndex_example
	:emphasize-lines: 1

	\id TDX
	\mt Subject Index
	\ip Introductory paragraph(s)
	...
	\s A
	\p \k Aaron\k*
	\xt Act 7.40
	\xt Heb 5.4; 7.11; 9.4
	...
	\p \k Angels\k*
	\pi (a) messengers and agents of God
	\xt Mat 1.20-24; 4.11; 13.39,41,49; 16.27; 34.31; 25.31; 28.2-7
	\xt Luk 1.11-19; 26-38; 2.9-21
	\xt Jhn 1.51
	...
	\pi (b) in heaven
	\xt Mat 22.30
	\xt Luk 12.8-9; 15.10; 20.36
	...

.. _usfm-book_NDX:
.. index:: names index, book; \id NDX

Names Index
^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\is# <usfmp_is#>` - Introduction heading.
* :ref:`\\ip <usfmp_ip>` - Introduction paragraph.
* :ref:`\\s# <usfmp_s#>` - Section heading (e.g. headings of alphabetical divisions - "A", "B", "C" etc.)
* :ref:`\\p <usfmp_p>` - Main entry *(required)*. May also be used for any additional paragraphs in the index entry (optional).
* :ref:`\\k ...\\k\* <usfmc_k>` - Main entry keyword *(required)*.
* :ref:`\\xt ...\\xt\* <usfmc_xt>` - Entry target reference(s) *(required)*. More than one \\xt ...\\xt\* entry can be provided to create logical groupings of references (per chapter; per book etc.).
* \\xtSee ...\\xtSee\* - Alternate entry target reference. (= custom Concordance and Names Index markup).
* \\xtSeeAlso ...\\xtSeeAlso\* - Additional entry target reference. (= custom Concordance and Names Index markup).

**Text Sample**

.. code-block:: text
	:name: periph-namesIndex_example
	:emphasize-lines: 1

	\id NDX
	\mt Names Index
	\ip Introductory paragraph(s) ...
	...
	\s A
	\p \k Aaron\k*
	\xt Exo 4.14-30 (x5)
	\xt Exo 5.1-21 (x5)
	...
	\p \k Abraham\k*
	\p See Also \xtSeeAlso Abram\xtSeeAlso*
	\xt Gen 17.5-27 (x8)
	\xt Gen 18.1-33 (x15)
	...
	\s B
	\p \k Baal\k*
	\xt Num 22.41
	\xt Num 25.3-5 (x2)