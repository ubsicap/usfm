.. include:: /_static/inc_styles.txt

.. index:: peripherals; introductions, introductions, book; \id INT

.. _usfm-book_INT:

Introductions
=============

The INT :doc:`book </identification/books>` and its :ref:`divisions <periph_div>` can be used for storing introductory material related to the various book groupings within a scripture publication. This material has also been referred to as "mid-matter". The following USFM markers are recommended for use in Introduction content.

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

**Text Sample**

.. code-block:: text
	:name: periph-introductions_example
	:emphasize-lines: 1,2,9,14,22,25,28,34,38,41,44

	\id INT
	\periph Old Testament Introduction
	\mt1 Introduction to the Old Testament
	\p The Old Testament is a record of Israel's experience of what God is like and what 
	the people who worship God should be like. It proclaims the LORD God as the creator of 
	the world and it tells how God blesses people and establishes relations with people 
	through special agreements called covenants.
	... 
	\periph Pentateuch Introduction
	\s1 The Pentateuch
	\p “Pentateuch” is a term that means “five scrolls (books)” and is used to describe the 
	five books that are positioned at the beginning of both Jewish and Christian Bibles.
	...
	\periph History Introduction
	\s1 Historical Books
	\p The books in this section describe important events in Israel's history. It begins 
	with descriptions of how the people entered Canaan, the land which God promised to 
	Abraham and Sarah and their descendants, and goes on to describe the time of Israel's 
	great kings (Saul, David, and Solomon) and the division of Israel into two kingdoms 
	(Israel in the north and Judah in the south) who often found themselves in conflict.
	... 
	\periph Poetry Introduction
	\s1 Books of Wisdom and Poetry
	...
	\periph Prophecy Introduction
	\s1 The Prophets
	...
	\periph Deuterocanon Introduction
	\mt1 Deuterocanonicals/Apocrypha
	\p Most of the books gathered in this section were part of an ancient translation of 
	the Hebrew Scriptures into Greek called the Septuagint which was widely read by 
	Christians in the early church.
	... 
	\periph New Testament Introduction
	\mt1 New Testament
	\p The books of the New Testament were written by the followers of Jesus Christ.
	...
	\periph Gospels Introduction
	\s1 Gospels and Acts
	...
	\periph Epistles Introduction
	\s1 The Letters of Paul
	...
	\periph Letters Introduction
	\s1 General Letters and Revelation
	...
