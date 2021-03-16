.. include:: /_static/inc_styles.txt

.. index:: titles, headings

Titles, Headings, and Labels
============================

.. _usfmp_mt#:
.. index:: marker; \mt#, titles; major title

\\mt#
^^^^^

:Syntax: ``\mt#_text...``
:Type: paragraph
:Added: 1.0
:Use: Major title. |br|
	The key components in the title of a biblical book. |br|
	The variable # represents a portion of the title, with the lesser emphasis (relative weighting) being on the higher numbers. |br|
	**\\mt = \\mt1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Samples** - Introduction to Acts (GNT)

.. code-block:: text
	:name: usfm-paragraph_mt#_example
	:emphasize-lines: 4-5

	\h Acts
	\toc1 The Acts of the Apostles
	\toc2 Acts
	\mt1 THE ACTS
	\mt2 of the Apostles
	\is Introduction
	\ip \bk The Acts of the Apostles\bk* is a continuation of \bk The Gospel according to Luke\bk*.

.. image:: images/usfm-paragraph_mt.jpg
	:width: 250px

Introduction to John (GNT)

.. code-block:: text
	:name: usfm-paragraph_mt#_example-alt
	:emphasize-lines: 4-6

	\h John
	\toc1 The Gospel according to John
	\toc2 John
	\mt2 The Gospel
	\mt3 according to
	\mt1 JOHN
	\is Introduction

.. image:: images/usfm-paragraph_mt-alt.jpg
	:width: 250px

-----

.. _usfmp_mte#:
.. index:: marker; \mte#, titles; major title at ending

\\mte#
^^^^^^

:Syntax: ``\mte#_text...``
:Type: paragraph
:Added: 1.0
:Use: Major title at ending. |br|
	May be used in texts which repeat the main title at the end of the introduction, or to mark a major title indicating the end of the introduction. |br|
	The content is not typically identical to :ref:`\\mt# <usfmp_mt#>`. |br|
	The variable # represents a portion of the title, with the lesser emphasis (relative weighting) being on the higher numbers. |br|
	**\\mte = \\mte1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Sample** - John

.. code-block:: text
	:name: usfm-paragraph_mte#_example
	:emphasize-lines: 1-2

	\mte2 The End of the Gospel according to
	\mte1 John

-----

.. _usfmp_ms#:
.. index:: marker; \ms#, headings; major section heading

\\ms#
^^^^^

:Syntax: ``\ms#_text...``
:Type: paragraph
:Added: 1.0
:Use: Major section heading. |br|
	These are headings before larger text divisions than what is typically considered a "section" division (see :ref:`\\s# <usfmp_s#>`). |br|
	The variable # represents the level of division. |br|
	**\\ms = \\ms1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Samples** - Psalm 1 (Book 1 division) (GNT)

.. code-block:: text
	:name: usfm-paragraph_ms#_example
	:emphasize-lines: 2

	\c 1
	\ms BOOK ONE
	\mr (Psalms 1–41)
	\s True Happiness
	\q1
	\v 1 Happy are those
	\q2 who reject the advice of evil people,

.. image:: images/usfm-paragraph_ms.jpg
	:width: 250px

Daniel 1.1 (GNT)

.. code-block:: text
	:name: usfm-paragraph_ms#_example-alt
	:emphasize-lines: 2

	\c 1
	\ms THE STORY OF DANIEL AND HIS FRIENDS
	\mr (1.1—6.28)
	\s The Young Men at Nebuchadnezzar's Court
	\p
	\v 1 In the third year that Jehoiakim was king of Judah, King Nebuchadnezzar of Babylonia 
	attacked Jerusalem and surrounded the city.

.. image:: images/usfm-paragraph_ms-alt.jpg
	:width: 250px


-----

.. _usfmp_mr:
.. index:: marker; \mr, headings; major section reference range

\\mr
^^^^

:Syntax: ``\mr_text...``
:Type: paragraph
:Added: 1.0
:Use: Major section reference range. |br|
	The text reference range listed under a major section heading.

**Text and Formatting Sample** - Psalm 1 (Book 1 division) (GNT)

.. code-block:: text
	:name: usfm-paragraph_mr_example
	:emphasize-lines: 3

	\c 1
	\ms BOOK ONE
	\mr (Psalms 1–41)
	\s True Happiness
	\q1
	\v 1 Happy are those
	\q2 who reject the advice of evil people,

.. image:: images/usfm-paragraph_mr.jpg
	:width: 250px

-----

.. _usfmp_s#:
.. index:: marker; \s#, headings; section heading

\\s#
^^^^

:Syntax: ``\s#_text...``
:Type: paragraph
:Added: 1.0
:Use: Section heading. |br|
	The typical (common) section division heading. |br|
	The variable # represents the level of division. |br|
	**\\s = \\s1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Samples** - Proverbs 22.17 (GNT)

.. code-block:: text
	:name: usfm-paragraph_s1_example
	:emphasize-lines: 1

	\s1 The Thirty Wise Sayings
	\p
	\v 17 Listen, and I will teach you what the wise have said. Study their teachings,
	\v 18 and you will be glad if you remember them and can quote them.
	\v 19 I want you to put your trust in the \nd Lord\nd*; that is why I am going to tell 
	them to you now.
	\v 20 I have written down thirty sayings for you. They contain knowledge and good advice,
	\v 21 and will teach you what the truth really is. Then when you are sent to find it 
	out, you will bring back the right answer.
	\s2 -1-
	\p
	\v 22 Don't take advantage of the poor just because you can; don't take advantage of 
	those who stand helpless in court.

.. image:: images/usfm-paragraph_s1.jpg
	:width: 250px

Proverbs 22.22,24 (GNT)

.. code-block:: text
	:name: usfm-paragraph_s2_example
	:emphasize-lines: 3,9

	\v 21 and will teach you what the truth really is. Then when you are sent to find it out, 
	you will bring back the right answer.
	\s2 -1-
	\p
	\v 22 Don't take advantage of the poor just because you can; don't take advantage of 
	those who stand helpless in court.
	\v 23 The \nd Lord\nd* will argue their case for them and threaten the life of anyone 
	who threatens theirs.
	\s2 -2-
	\p
	\v 24 Don't make friends with people who have hot, violent tempers.
	\v 25 You might learn their habits and not be able to change.

.. image:: images/usfm-paragraph_s2.jpg
	:width: 250px

-----

.. _usfmp_sr:
.. index:: marker; \sr, headings; section reference range

\\sr
^^^^

:Syntax: ``\sr_text...``
:Type: paragraph
:Added: 2.0
:Use: Section reference range. |br|
	The text reference range listed under a section heading. |br|
	\\sr is not equivalent to \\r which is used for marking parallel references. |br|
	|ico_See| *See also* :ref:`\\mr <usfmp_mr>`

**Text and Formatting Sample** - Proverbs 22.17 (GNT - *markup adapted*)

.. code-block:: text
	:name: usfm-paragraph_sr_example
	:emphasize-lines: 2

	\s1 The Thirty Wise Sayings
	\sr (22.17--24.22)
	\p
	\v 17 Listen, and I will teach you what the wise have said. Study their teachings, ...

.. image:: images/usfm-paragraph_sr.jpg
	:width: 250px

-----

.. _usfmp_r:
.. index:: marker; \r, headings; parallel passage references

\\r
^^^

:Syntax: ``\r_text...``
:Type: paragraph
:Added: 1.0
:Use: Parallel passage reference(s). |br|
	A reference to a parallel passage usually located under a section heading :ref:`\\s# <usfmp_s#>`.

**Text and Formatting Sample** - Matthew 3.1 (GNT)

.. code-block:: text
	:name: usfm-paragraph_r_example
	:emphasize-lines: 3

	\c 3
	\s1 The Preaching of John the Baptist
	\r (Mark 1.1-8; Luke 3.1-18; John 1.19-28)
	\p
	\v 1 At that time John the Baptist came to the desert of Judea and started preaching.
	\v 2 “Turn away from your sins,” he said, ...

.. image:: images/usfm-paragraph_r.jpg
	:width: 250px

-----

.. _usfmc_rq:
.. index:: marker; \rq ...\rq*, headings; inline quotation references

\\rq ...\\rq\*
^^^^^^^^^^^^^^

:Syntax: ``\rq ...\rq*``
:Type: character
:Added: 1.0
:Use: Inline quotation reference(s). |br|
	A reference indicating the source text for the preceding quotation (usually an Old Testament quote).

.. note::
	\\rq ...\\rq* reference(s) are intended to be formatted (typeset) within the scripture body text column, and not extracted from the text as are regular cross references (:ref:`\\x ...\\x* <usfmn_x>`). They are also typically separated from the main text of Scripture using a different type style and alignment.

**Text and Formatting Sample** - Hebrews 1.5 (GNT)

.. code-block:: text
	:name: usfm-character_rq_example
	:emphasize-lines: 7,12

	\p
	\v 4 The Son was made greater than the angels, just as the name that God gave him is greater 
	than theirs.
	\v 5 For God never said to any of his angels,
	\q1 "You are my Son;
	\q2 today I have become your Father."
	\rq Psa 2.7\rq*
	\b
	\m Nor did God say about any angel,
	\q1 "I will be his Father,
	\q2 and he will be my Son."
	\rq 2Sa 7.14; 1Ch 17.13\rq*

.. image:: images/usfm-character_rq.jpg
	:width: 250px

-----

.. _usfmp_d:
.. index:: marker; \d, headings; descriptive title

\\d
^^^

:Syntax: ``\d_text...``
:Type: paragraph
:Added: 1.0
:Use: Descriptive title (or "Hebrew subtitle"). |br|
	Sometimes used in Psalms under the section heading (e.g. "For the director of Music").

**Text and Formatting Sample** - Psalm 3.1 (NRSV)

.. code-block:: text
	:name: usfm-paragraph_d_example
	:emphasize-lines: 3

	\c 3
	\s1 Trust in God under Adversity
	\d A Psalm of David, when he fled from his son Absalom.
	\q1
	\v 1 O \nd Lord\nd*, how many are my foes!
	\q2 Many are rising against me;
	\q1
	\v 2 many are saying to me,
	\q2 “There is no help for you in God.” \qs Selah\qs*

.. image:: images/usfm-paragraph_d.jpg
	:width: 250px

-----

.. _usfmp_sp:
.. index:: marker; \sp, labels; speaker

\\sp
^^^^

:Syntax: ``\sp_text...``
:Type: paragraph
:Added: 1.0
:Use:  Speaker Identification (e.g. Job and Song of Songs).

**Text and Formatting Sample** - Job 3.1 (GNT)

.. code-block:: text
	:name: usfm-paragraph_sp_example
	:emphasize-lines: 5

	\c 3
	\s1 Job's Complaint to God
	\p
	\v 1 Finally Job broke the silence and cursed the day on which he had been born.
	\sp Job
	\q1
	\v 2-3 O God, put a curse on the day I was born;
	\q2 put a curse on the night when I was conceived!

.. image:: images/usfm-paragraph_sp.jpg
	:width: 250px

-----

.. _usfmp_sd#:
.. index:: marker; \sd#, labels; semantic division

\\sd#
^^^^^

|badge_3.0|

:Syntax: ``\sd#``
:Type: paragraph
:Added: 3.0
:Use: Semantic division (semantic space). |br|
	Vertical space used to divide the text into sections, in a manner similar to the structure added through the use of a sequence of heading texts (i.e. :ref:`\\ms# <usfmp_ms#>` and :ref:`\\s# <usfmp_s#>`). |br|
	The purpose of ``\sd#`` is distinct from :ref:`\\b <usfmp_b>` which primarily denotes whitespace (and in particular at poetic stanza breaks) and not hierarchy or division.
	The variable # represents the level of division being marked. |br|
	**\\sd = \\sd1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Sample** - Matthew 13.51-54 (NIV "Books of the Bible"; chapter and verse numbers suppressed in layout; new sections begin with drop capital)

.. code-block:: text
	:name: usfm-paragraph_sd_example
	:emphasize-lines: 8

	\m
	\v 51 “Have you understood all these things?” Jesus asked.
	\p “Yes,” they replied.
	\p
	\v 52 He said to them, “Therefore every teacher of the law who has been instructed about 
	the kingdom of heaven is like the owner of a house who brings out of his storeroom new 
	treasures as well as old.”
	\sd2
	\p
	\v 53 When Jesus had finished these parables, he moved on from there.
	\v 54 Coming to his hometown, he began teaching the people in their synagogue, and they 
	were amazed. “Where did this man get this wisdom and these miraculous powers?” they asked. 		

.. image:: images/usfm-paragraph_sd.jpg
	:width: 350px
