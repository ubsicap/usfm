.. include:: /_static/inc_styles.txt

.. index:: study content; footnotes, extended footnotes, study note

Extended Footnotes
==================

.. index:: extended footnote; container, study note; container

.. rubric:: Extended Footnote Container

The **extended footnotes** are inserted in-line within the study project text using the following general syntax. The boundaries of the footnote text are defined by an opening and closing marker. The remainder of the note is written using standard USFM :ref:`footnote content elements <usfmn_f-content>` markers.

.. _usfmn_ef:
.. index:: marker; \ef ...\ef*, footnote; study note

\\ef ...\\ef\*
--------------

:Syntax: ``\ef_+_(\fr_REF_)footnote content\ef*``
:Type: extended note
:Added: 2.1
:Use: Beginning and ending of the extended footnote element.

:red:`+`

* The extended footnote caller, which may be one of the following three types:

	    :red:`+` – indicates that the caller should be generated automatically by the translation editor, or publishing tools. |br|
	    :red:`-` – indicates that no caller should be generated, and is not used. |br|
	    :red:`?` – where ? represents the character to be used for the caller. The caller is defined for the specific note by the author.			

:red:`footnote content`

	* All of the text elements which make up the extended footnote. Refer to the documentation on using standard USFM :ref:`footnote content element <usfmn_f-content>` markers.
	* The :ref:`\\xt <usfmc_xt>` (cross reference target) element can be used for the purpose of marking references within note text to other scripture or note passages
	* Other standard USFM character level markup may be included, such as:
	
		- :ref:`\\w <usfmc_w>` - Wordlist/Glossary/Dictionary reference
		- :ref:`\\nd <usfmc_nd>`, :ref:`\\bk <usfmc_bk>`, :ref:`\\tl <usfmc_tl>`, :ref:`\\pn <usfmc_pn>` - Name of Deity, Quoted book title, Transliterated word, Proper name

-----

.. rubric:: Text and Formatting Samples

Mark 1.1-5 (GNSB)

.. code-block:: text
	:name: usfm-study_efnotes_example
	:emphasize-lines: 2-3,5-8,14-15,17-20,22-23,25-26

	\p
	\v 1 This is the Good News about Jesus Christ, the Son of God\ef - \fr 1.1: \fq the Son 
	of God: \ft Not included in some manuscripts.\ef*.\f + \fr 1.1 \ft Some manuscripts do 
	not have \fq the Son of God.\f*
	\v 2 \ef - \fr 1.2: \fk Prophet\ef*It began as the prophet Isaiah had written\ef - \fr 1.2: 
	\fq Isaiah had written: \ft The quotation in 1.2 is from Mal 3.1; “ahead of you” may be 
	from Ex 23.20, “Someone is shouting in the desert, ‘Get the road ready for the Lord; make 
	a straight path for our God to travel!’ ”.\ef*:\x - \xo 1.2: \xt Mal 3.1\x*
	\q1 “God said, ‘I will send my messenger ahead of you
	\q2 to clear the way for you.’
	\q1
	\v 3 Someone is shouting in the desert,\x - \xo 1.3: \xt Is 40.3 (LXX)\x*
	\q2 ‘Get the road ready for the Lord;
	\q2 make a straight path for him to travel\ef - \fr 1.3: \fq someone is…travel: \ft is from 
	Is 40.3, following Septuagint; the Hebrew means, “Get the road ready in the desert”.\ef*!’”
	\p
	\v 4 \ef - \fr 1.4: \fk Baptizing\ef*So John appeared\ef - \fr 1.4: \fq John appeared: 
	\ft John probably began his ministry in AD 27 (Lk 3.1-3).\ef* in the desert\ef - \fr 1.4: 
	\fq the desert: \ft The desolate region on the west side of the River Jordan, not far from 
	where it empties into the Dead Sea.\ef*, baptizing and preaching.\f + \fr 1.4 \fq John 
	appeared in the desert, baptizing and preaching; \ft some manuscripts have \fq John the 
	Baptist appeared in the desert, preaching.\f*\ef - \fr 1.4: \fq John…baptizing and 	preaching: 
	\ft Some manuscripts have “John the Baptist appeared in the desert, preaching”.\ef* “Turn 
	away from your sins and be baptized,” he told the people, “and God will forgive your sins.”
	\v 5 Many people from the province of Judea\ef - \fr 1.5: \fq Judea: \ft One of the 
	provinces, in the south, into which the land of Israel was then divided.\ef* and the city 
	of Jerusalem went out to hear John. They confessed their sins, and he baptized them in 
	the River Jordan.
	...

.. image:: images/usfm-study_efnotes.jpg
	:width: 300px
