.. include:: /_static/inc_styles.txt

.. index:: peripherals; front matter, front matter, book; \id FRT

.. _usfm-book_FRT:

Front Matter
============

The FRT :doc:`book </identification/books>` and its :ref:`divisions <periph_div>` can be used for storing various material which is typically presented at the start of a scripture publication, before the first book of scripture.

.. index:: periph; Title Page, title page

\\periph Title Page
^^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\pc <usfmp_pc>` - Centered paragraph.
* :ref:`\\fig ...\\fig\* <usfmc_fig>` - Figure. 

**Text Sample**

.. code-block:: text
	:name: periph-titlePage_example
	:emphasize-lines: 3

	\id FRT
	...
	\periph Title Page 
	\mt1 Holy Bible 
	\mt3 with 
	\mt2 Deuterocanonicals/Apocrypha 
	\pc Good News Translation
	\pc \fig |gntLogo.jpg|span||||\fig* 
	\pc \fig |absLogo.jpg|span||||\fig*
	\pc American Bible Society

.. index:: periph; Half Title Page, half title page

\\periph Half Title Page
^^^^^^^^^^^^^^^^^^^^^^^^

* :ref:`\mt# <usfmp_mt#>` - Main title.
* :ref:`\pc <usfmp_pc>` - Centered paragraph.
* :ref:`\\fig ...\\fig\* <usfmc_fig>` - Figure.

**Text Sample**

.. code-block:: text
	:name: periph-halfTitlePage_example
	:emphasize-lines: 3

	\id FRT
	...
	\periph Half Title Page
	\mt1 Holy Bible
	\pc Good News Translation
	\pc \fig |gntLogo.jpg|span||||\fig*

.. index:: periph; Promotional Page, promotional page

\\periph Promotional Page
^^^^^^^^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\p <usfmp_p>` - Paragraph.
* :ref:`\\m <usfmp_m>` - Flush left (margin) paragraph.
* :ref:`\\pi# <usfmp_pi#>` - Indented paragraph.
* :ref:`\\li# <usfmp_li#>` - List item.
* :ref:`\\q# <usfmp_q#>` - Poetic line.

.. index:: periph; Imprimatur, imprimatur

\\periph Imprimatur
^^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\pc <usfmp_pc>` - Centered paragraph.
* :ref:`\\p <usfmp_p>` - Paragraph.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.
* :ref:`\\fig ...\\fig\* <usfmc_fig>` - Figure.

.. index:: periph; Publication Data, publication data

\\periph Publication Data
^^^^^^^^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\pc <usfmp_pc>` - Centered paragraph.
* :ref:`\\p <usfmp_p>` - Paragraph.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.

.. index:: periph; Foreword, foreword

\\periph Foreword
^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\p <usfmp_p>` - Paragraph.
* :ref:`\\m <usfmp_m>` - Flush left (margin) paragraph.
* :ref:`\\pi# <usfmp_pi#>` - Indented paragraph.
* :ref:`\\li# <usfmp_li#>` - List item.
* :ref:`\\q# <usfmp_q#>` - Poetic line.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.
* :ref:`\\bk ...\\bk\* <usfmc_bk>`, :ref:`\\qt ...\\qt\* <usfmc_qt>`, :ref:`\\tl ...\\tl\* <usfmc_tl>` or other character styles
* :ref:`\\fig ...\\fig\* <usfmc_fig>` - Figure.

.. index:: periph; Preface, preface

\\periph Preface
^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\p <usfmp_p>` - Paragraph.
* :ref:`\\m <usfmp_m>` - Flush left (margin) paragraph.
* :ref:`\\pi# <usfmp_pi#>` - Indented paragraph.
* :ref:`\\li# <usfmp_li#>` - List item.
* :ref:`\\q# <usfmp_q#>` - Poetic line.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.
* :ref:`\\bk ...\\bk\* <usfmc_bk>`, :ref:`\\qt ...\\qt\* <usfmc_qt>`, :ref:`\\tl ...\\tl\* <usfmc_tl>` or other character styles
* :ref:`\\fig ...\\fig\* <usfmc_fig>` - Figure.

.. index:: periph; Table of Contents, table of contents

\\periph Table of Contents
^^^^^^^^^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.

**Text Sample**

In the following example, the variable # represents the location of a page number, to be inserted during the typesetting process.

.. code-block:: text
	:name: periph-tableOfContents_example
	:emphasize-lines: 3

	\id FRT
	...
	\periph Table of Contents
	\mt Contents
	\s Old Testament
	\tr  \th1 Name  \thr2 Page \th3 Name \thr4 Page 
	\tr \tc1 Genesis \tcr2 # \tc3 Ecclesiastes \tcr4 #
	\tr \tc1 Exodus \tcr2 # \tc3 Song of Songs \tcr4 #
	\tr \tc1 Leviticus \tcr2 # \tc3 Isaiah \tcr4 #
	...
	\s New Testament
	\tr  \th1 Name  \thr2 Page \th3 Name \thr4 Page
	\tr \tc1 Matthew \tcr2 # \tc3 1 Timothy \tcr4 #

.. index:: periph; Alphabetical Contents, alphabetical contents

\\periph Alphabetical Contents
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.

.. index:: periph; Table of Abbreviations, table of abbreviations

\\periph Table of Abbreviations
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* :ref:`\\mt# <usfmp_mt#>` - Main title.
* :ref:`\\s# <usfmp_s#>` - Section heading.
* :ref:`\\tr <usfmp_tr>`, :ref:`\\th# <usfmc_th#>`, :ref:`\\thr# <usfmc_thr#>`, :ref:`\\tc# <usfmc_tc#>`, :ref:`\\tcr# <usfmc_tcr#>`  - For any tabular data.

**Text Sample**

.. code-block:: text
	:name: periph-tableOfAbbreviations_example
	:emphasize-lines: 3

	\id FRT
	...
	\periph Table of Abbreviations 
	\mt1 Alphabetical List of Biblical Books and Abbreviations 
	\tr  \th1 Name \th2 Abbrev.  \thr3 Page 
	\tr  \tc1 Acts \tc2 Ac \tcr3 #
	\tr  \tc1 Amos \tc2 Am \tcr3 #
	\tr  \tc1 1 Chronicles \tc2 1Ch \tcr3 #
	\tr  \tc1 2 Chronicles \tc2 2Ch \tcr3 #
	\tr  \tc1 Colossians \tc2 Col \tcr3 #
	\tr  \tc1 1 Corinthians \tc2 1Co \tcr3 #
	\tr  \tc1 2 Corinthians \tc2 2Co \tcr3 #
	\tr  \tc1 Daniel \tc2 Dn \tcr3 #
	\tr  \tc1 Deuteronomy \tc2 Dt \tcr3 #
	\tr  \tc1 Ecclesiastes \tc2 Ec \tcr3 #
	\tr  \tc1 Ephesians \tc2 Eph \tcr3 #
	\tr  \tc1 Esther \tc2 Es \tcr3 #
	...
	\s1 Other Abbreviations
	\tr  \tc1 Circa (around) \tc2 c \tc3 #
	\tr  \tc1 Old Testament \tc2 OT \tc3 #
	\tr  \tc1 New Testament \tc2 NT \tc3 #
	\tr  \tc1 Septuagint \tc2 LXX \tc3 #