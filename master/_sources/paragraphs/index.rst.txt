.. include:: /_static/inc_styles.txt

.. index:: paragraphs

Paragraphs
==========

.. _usfmp_p:
.. index:: marker; \p, paragraphs; normal

\\p
^^^

:Syntax: ``\p(_text...)``
:Type: paragraph
:Added: 1.0
:Use: Normal paragraph. |br|
	Followed immediately by a space and paragraph text, or by a new line and a verse marker.

**Text and Formatting Sample** - Mark 1.1-4 (GNT)

.. code-block:: text
	:name: usfm-paragraph_p_example
	:emphasize-lines: 4,13

	\c 1
	\s1 The Preaching of John the Baptist
	\r (Matthew 3.1-12; Luke 3.1-18; John 1.19-28)
	\p
	\v 1 This is the Good News about Jesus Christ, the Son of God.
	\v 2 It began as the prophet Isaiah had written:
	\q1 “God said, ‘I will send my messenger ahead of you
	\q2 to open the way for you.’
	\q1
	\v 3 Someone is shouting in the desert,
	\q2 ‘Get the road ready for the Lord;
	\q2 make a straight path for him to travel!’”
	\p
	\v 4 So John appeared in the desert, baptizing and preaching. “Turn away from your sins 
	and be baptized,” he told the people, “and God will forgive your sins.”

.. image:: images/usfm-paragraph_p.jpg
	:width: 250px

-----

.. _usfmp_m:
.. index:: marker; \m, paragraphs; margin

\\m
^^^

:Syntax: ``\m(_text...)``
:Type: paragraph
:Added: 1.0
:Use: Continuation (margin) paragraph. |br|
	No first line indent. |br|
	Followed immediately by a space and paragraph text, or by a new line and a verse marker. |br|
	Usually used to resume prose at the margin (without indent) after poetry or OT quotation (i.e. continuation of the previous paragraph).

**Text and Formatting Sample** - Mark 12.37 (GNT)

.. code-block:: text
	:name: usfm-paragraph_m_example
	:emphasize-lines: 9

	\p
	\v 35 As Jesus was teaching in the Temple, he asked the question, “How can the teachers 
	of the Law say that the Messiah will be the descendant of David?
	\v 36 The Holy Spirit inspired David to say:
	\q1 ‘The Lord said to my Lord:
	\q2 Sit here at my right side
	\q2 until I put your enemies under your feet.’
	\b
	\m
	\v 37 David himself called him ‘Lord’; so how can the Messiah be David's descendant?”

.. image:: images/usfm-paragraph_m.jpg
	:width: 250px

-----

.. _usfmp_po:
.. index:: marker; \po, paragraphs; letter opening

\\po
^^^^

|badge_3.0|

:Syntax: ``\po_text...``
:Type: paragraph
:Added: 3.0
:Use: Opening of an epistle/letter.

**Text and Formatting Sample** - Romans 1.1,7 (GNT)

.. code-block:: text
	:name: usfm-paragraph_po_example
	:emphasize-lines: 2,15,18

	\c 1
	\po
	\v 1 From Paul, a servant of Christ Jesus and an apostle chosen and called by God to 
	preach his Good News.
	\p
	\v 2 The Good News was promised long ago by God through his prophets, as written in the 
	Holy Scriptures.
	\v 3 It is about his Son, our Lord Jesus Christ: as to his humanity, he was born a 
	descendant of David;
	\v 4 as to his divine holiness, he was shown with great power to be the Son of God by being 
	raised from death.
	\v 5 Through him God gave me the privilege of being an apostle for the sake of Christ, 
	in order to lead people of all nations to believe and obey.
	\v 6 This also includes you who are in Rome, whom God has called to belong to Jesus Christ.
	\po
	\v 7 And so I write to all of you in Rome whom God loves and has called to be his own 
	people:
	\po May God our Father and the Lord Jesus Christ give you grace and peace. 

.. image:: images/usfm-paragraph_po.jpg
	:width: 450px

-----

.. _usfmp_pr:
.. index:: marker; \pr, paragraphs; right-aligned, paragraphs; text refrain

\\pr
^^^^

:Syntax: ``\pr(_text...)``
:Type: paragraph
:Added: 1.0
:Deprecated: 2.0
:Restored: 3.0 |badge_3.0|
:Use: Right-aligned paragraph. |br|
	|ico_Cg| *Recommended use:* Text refrain.

**Text and Formatting Sample** - Deuteronomy 27.15,16,17 (GNT - *markup adapted*)

.. code-block:: text
	:name: usfm-paragraph_pr_example
	:emphasize-lines: 4,7,10

	\p
	\v 15 “ ‘God's curse on anyone who makes an idol of stone, wood, or metal and secretly 
	worships it; the \nd Lord\nd* hates idolatry.’
	\pr “And all the people will answer, ‘Amen!’
	\p
	\v 16 “ ‘God's curse on anyone who dishonors his father or mother.’
	\pr “And all the people will answer, ‘Amen!’
	\p
	\v 17 “ ‘God's curse on anyone who moves a neighbor's property line.’
	\pr “And all the people will answer, ‘Amen!’

.. image:: images/usfm-paragraph_pr.jpg
	:width: 250px

-----

.. _usfmp_cls:
.. index:: marker; \cls, paragraphs; letter closing

\\cls
^^^^^

:Syntax: ``\cls_text...``
:Type: paragraph
:Added: 1.0
:Use: Closure of an epistle/letter. |br|
	Similar to "With love," or "Sincerely yours,".

**Text and Formatting Sample** - Colossians 4.18 (GNT - *markup adapted*)

.. code-block:: text
	:name: usfm-paragraph_cls_example
	:emphasize-lines: 3

	\p
	\v 18 With my own hand I write this: \sig Greetings from Paul\sig*. Do not forget my chains!
	\cls May God's grace be with you.

.. image:: images/usfm-paragraph_cls.jpg
	:width: 250px

-----

.. _usfmp_pmo:
.. index:: marker; \pmo, paragraphs; embedded text opening

\\pmo
^^^^^

:Syntax: ``\pmo(_text...)``
:Type: paragraph
:Added: 2.0
:Use: Embedded text opening. |br|

**Text and Formatting Sample** - Acts 15.24 (CEV)

.. code-block:: text
	:name: usfm-paragraph_pmo_example
	:emphasize-lines: 6

	\p
	\v 22 The apostles, the leaders, and all the church members decided to send some men to 
	Antioch along with Paul and Barnabas. They chose Silas and Judas Barsabbas, who were two 
	leaders of the Lord's followers.
	\v 23 They wrote a letter that said:
	\pmo We apostles and leaders send friendly greetings to all of you Gentiles who are 
	followers of the Lord in Antioch, Syria, and Cilicia.
	\pm
	\v 24 We have heard that some people from here have terribly upset you by what they said. 
	But we did not send them!

.. image:: images/usfm-paragraph_pmo.jpg
	:width: 250px

-----

.. _usfmp_pm:
.. index:: marker; \pm, paragraphs; embedded text

\\pm
^^^^

:Syntax: ``\pm(_text...)``
:Type: paragraph
:Added: 2.0
:Use: Embedded text paragraph. |br|

**Text and Formatting Sample** - Act 15.24-27,28-29 (CEV)

.. code-block:: text
	:name: usfm-paragraph_pm_example
	:emphasize-lines: 3,11

	\pmo We apostles and leaders send friendly greetings to all of you Gentiles who are 
	followers of the Lord in Antioch, Syria, and Cilicia.
	\pm
	\v 24 We have heard that some people from here have terribly upset you by what they said. 
	But we did not send them!
	\v 25 So we met together and decided to choose some men and to send them to you along with 
	our good friends Barnabas and Paul.
	\v 26 These men have risked their lives for our Lord Jesus Christ.
	\v 27 We are also sending Judas and Silas, who will tell you in person the same things that 
	we are writing.
	\pm
	\v 28 The Holy Spirit has shown us that we should not place any extra burden on you...

.. image:: images/usfm-paragraph_pm.jpg
	:width: 250px

-----

.. _usfmp_pmc:
.. index:: marker; \pmc, paragraphs; embedded text closing

\\pmc
^^^^^

:Syntax: ``\pmc(_text...)``
:Type: paragraph
:Added: 2.0
:Use: Embedded text closing. |br|

**Text and Formatting Sample** - Act 15.28-29 (CEV)

.. code-block:: text
	:name: usfm-paragraph_pmc_example
	:emphasize-lines: 6

	\pm
	\v 28 The Holy Spirit has shown us that we should not place any extra burden on you.
	\v 29 But you should not eat anything offered to idols. You should not eat any meat that 
	still has the blood in it or any meat of any animal that has been strangled. You must also 
	not commit any terrible sexual sins. If you follow these instructions, you will do well.
	\pmc We send our best wishes.

.. image:: images/usfm-paragraph_pmc.jpg
	:width: 250px

-----

.. _usfmp_pmr:
.. index:: marker; \pmr, paragraphs; embedded text refrain

\\pmr
^^^^^

:Syntax: ``\pmr_text...``
:Type: paragraph
:Added: 2.0
:Use: 	Embedded text refrain.

-----

.. _usfmp_pi#:
.. index:: marker; \pi#, paragraphs; indented

\\pi#
^^^^^

:Syntax: ``\pi#(_Sample text...)``
:Type: paragraph
:Added: 1.0
:Use: Indented paragraph. |br|
	Used in some texts for discourse sections. |br|
	The variable # represents the level of indent. |br|
	|ico_See| *See also* :ref:`\\pm <usfmp_pm>` |br|
	**\\pi = \\pi1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Sample** - Matthew 13.37-39 (CEV)

.. code-block:: text
	:name: usfm-paragraph_pi#_example
	:emphasize-lines: 7

	\s1 Jesus Explains the Story about the Weeds
	\p
	\v 36 After Jesus left the crowd and went inside, his disciples came to him and said, 
	“Explain to us the story about the weeds in the wheat field.”
	\p
	\v 37 Jesus answered:
	\pi The one who scattered the good seed is the Son of Man.
	\v 38 The field is the world, and the good seeds are the people who belong to the kingdom. 
	The weed seeds are those who belong to the evil one,
	\v 39 and the one who scattered them is the devil. The harvest is the end of time, and 
	angels are the ones who bring in the harvest.

.. image:: images/usfm-paragraph_pi.jpg
	:width: 250px

-----

.. _usfmp_mi:
.. index:: marker; \mi, paragraphs; indented margin

\\mi
^^^^

:Syntax: ``\mi(_text...)``
:Type: paragraph
:Added: 1.0
:Use: Indented flush left paragraph. |br|
	No first line indent. |br|
	|ico_See| *See also* :ref:`\\pmo <usfmp_pmo>`, :ref:`\\pmc <usfmp_pmc>`

**Text and Formatting Sample** - Matthew 11.18-19 (CEV)

.. code-block:: text
	:name: usfm-paragraph_mi_example
	:emphasize-lines: 10

	\pi
	\v 16 You people are like children sitting in the market and shouting to each other,
	\b
	\q1
	\v 17 “We played the flute,
	\q2 but you would not dance!
	\q1 We sang a funeral song,
	\q2 but you would not mourn!”
	\b
	\mi
	\v 18 John the Baptist did not go around eating and drinking, and you said, “That man has 
	a demon in him!”
	\v 19 But the Son of Man goes around eating and drinking, and you say, “That man eats and 
	drinks too much! He is even a friend of tax collectors ...

.. image:: images/usfm-paragraph_mi.jpg
	:width: 250px

-----

.. _usfmp_nb:
.. index:: marker; \nb, paragraphs; no-break

\\nb
^^^^

:Syntax: ``\nb``
:Type: paragraph
:Added: 1.0
:Use: Basic. |br|
	Indicates "no-break" with previous paragraph (regardless of previous paragraph type). |br|
	Commonly used in cases where the previous paragraph spans the chapter boundary.

**Text and Formatting Sample** - John 7.53–8.2 (CEV)

.. code-block:: text
	:name: usfm-paragraph_nb_example
	:emphasize-lines: 8

	\p
	\v 52 Then they said, “Nicodemus, you must be from Galilee! Read the Scriptures, and you 
	will find that no prophet is to come from Galilee.”
	\s1 A Woman Caught in Sin
	\p
	\v 53 Everyone else went home,
	\c 8
	\nb
	\v 1 but Jesus walked out to the Mount of Olives.
	\v 2 Then early the next morning he went to the temple. The people came to him, and he 
	sat down and started teaching them.

.. image:: images/usfm-paragraph_nb.jpg
	:width: 250px

.. note::

	**No-break markup within poetry:** Some translations have a publishing tradition of inserting a small amount of additional white-space at chapter boundaries. It is important in these texts to use the \nb marker within any specific poetic contexts where no visible break in the flow of the the text is intended at a particular chapter boundary.

-----

.. _usfmp_pc:
.. index:: marker; \pc, paragraphs; centered

\\pc
^^^^

:Syntax: ``\pc(_text...)``
:Type: paragraph
:Added: 1.0
:Use: Centered paragraph. |br| |br|
	|ico_Cg| *Recommended use:* Inscriptions. |br|

**Text and Formatting Sample** - Revelation 17.5 (CEV)

.. code-block:: text
	:name: usfm-paragraph_pc_example
	:emphasize-lines: 5

	\v 4 The woman was dressed in purple and scarlet robes, and she wore jewelry made of 
	gold, precious stones, and pearls. In her hand she held a gold cup filled with the filthy 
	and nasty things she had done.
	\v 5 On her forehead a mysterious name was written:
	\pc I AM THE GREAT CITY OF BABYLON, THE MOTHER OF EVERY IMMORAL AND FILTHY THING ON EARTH.
	\m
	\v 6 I could tell that the woman was drunk on the blood of God's people who had given 
	their lives for Jesus. This surprising sight amazed me, ...

.. image:: images/usfm-paragraph_pc.jpg
	:width: 250px

-----

.. _usfmp_ph#:
.. index:: marker; \ph#, paragraphs; hanging indent

\\ph#
^^^^^

:Syntax: ``\ph#(_text...)``
:Type: paragraph
:Added: 1.0
:Use: Indented paragraph with hanging indent. |br|
	The variable # represents the level of overall paragraph indent. |br|
	**\\ph = \\ph1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers) |br|
	**Deprecated** (i.e. use is strongly discouraged). |br| |br|
	|ico_Cg| *Recommended alternate:* :ref:`\\li# <usfmp_li#>`

-----

.. _usfmp_b-alt:
.. index:: marker; \b, paragraphs; blank line

\\b
^^^

:Syntax: ``\b``
:Type: paragraph
:Added: 1.0
:Use: Blank line. |br|
	May be used to explicitly indicate additional white space between paragraphs. |br|
	|ico_See| *See also:* Poetry elements :ref:`\\b <usfmp_b>` (used for stanza breaks in poetry, or between poetry and prose).

.. warning::

	No text should follow this marker, and it should not be used before or after titles to indicate white-space.