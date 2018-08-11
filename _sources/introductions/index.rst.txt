.. include:: /_static/inc_styles.txt

.. index:: introductions

Introductions
=============

.. _usfmp_imt#:
.. index:: marker; \imt#, introductions; major title

\\imt#
^^^^^^

:Syntax: ``\imt#_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction major title. |br|
	The variable # denotes the title level or relative weighting. |br|
	**\\imt = \\imt1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers) |br| |br|
	|ico_Cg| *Recommended use* is for the introduction title or other major introduction division (rather than :ref:`\\is <usfmp_is#>`) when the introduction text contains numerous additional sub-divisions.

**Text and Formatting Sample** - Introduction to Mark (RVE)

.. code-block:: text
	:name: usfm-paragraph_imt#_example
	:emphasize-lines: 4

	\h SAN MARCOS
	\mt2 Evangelio según
	\mt1 SAN MARCOS
	\imt1 INTRODUCCIÓN
	\is1 Importancia del evangelio de Marcos
	\ip Este evangelio, segundo de los libros del NT, contiene poco material que no aparezca 
	igualmente en \bk Mateo\bk* y \bk Lucas.\bk*

.. image:: images/usfm-paragraph_imt.jpg
	:width: 250px

-----

.. _usfmp_is#:
.. index:: marker; \is#, introductions; section heading

\\is#
^^^^^

:Syntax: ``\is#_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction section heading. |br|
	The variable # denotes the title level or relative weighting. |br|
	**\\is = \\is1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Sample** - Introduction to Mark (RVE)

.. code-block:: text
	:name: usfm-paragraph_is#_example
	:emphasize-lines: 5

	\h SAN MARCOS
	\mt2 Evangelio según
	\mt1 SAN MARCOS
	\imt1 INTRODUCCIÓN
	\is1 Importancia del evangelio de Marcos
	\ip Este evangelio, segundo de los libros del NT, contiene poco material que no aparezca 
	igualmente en \bk Mateo\bk* y \bk Lucas\bk*.

.. image:: images/usfm-paragraph_is.jpg
	:width: 250px

-----

.. _usfmp_ip:
.. index:: marker; \ip, introductions; paragraph

\\ip
^^^^

:Syntax: ``\ip_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction paragraph. |br|

**Text and Formatting Sample** - Introduction to Mark (GNT)

.. code-block:: text
	:name: usfm-paragraph_ip_example
	:emphasize-lines: 5

	\h Mark
	\mt2 The Gospel according to
	\mt1 MARK
	\is Introduction
	\ip \bk The Gospel according to Mark\bk* begins with the statement that it is “the Good News 
	about Jesus Christ, the Son of God.” Jesus is pictured as a man of action and authority. His 
	authority is seen in his teaching, in his power over demons, and in forgiving people's sins. 
	Jesus speaks of himself as the Son of Man, who came to give his life to set people free from sin.

.. image:: images/usfm-paragraph_ip.jpg
	:width: 300px

-----

.. _usfmp_ipi:
.. index:: marker; \ipi, introductions; indented paragraph

\\ipi
^^^^^

:Syntax: ``\ipi_text...``
:Type: paragraph
:Added: 1.0
:Use: Indented introduction paragraph. |br|

**Text and Formatting Sample** - Introduction to the Deuterocanonicals/Apocrypha (GCEV)

.. code-block:: text
	:name: usfm-paragraph_ipi_example
	:emphasize-lines: 3,5

	\ip The following lists summarize each Christian tradition’s views of the books here designated 
	as Deuterocanonicals/Apocrypha.
	\ipi Many Protestants consider the following books to be Apocrypha as defined above: Tobit, 
	Judith, additions to Esther (as found in Greek Esther in the CEV) ...
	\ipi Roman Catholics consider the following books to be Deuterocanonical and of equal status 
	with all other books of the Old Testament: Tobit, Judith, Greek Esther ...

.. image:: images/usfm-paragraph_ipi.jpg
	:width: 250px

-----

.. _usfmp_im:
.. index:: marker; \im, introductions; margin paragraph

\\im
^^^^

:Syntax: ``\im_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction flush left (margin) paragraph. |br|

**Text and Formatting Sample** - Introduction to the GCEV

.. code-block:: text
	:name: usfm-paragraph_im_example
	:emphasize-lines: 7

	\imt1 Preface:
	\is1 A Word about the Contemporary English Version
	\imi \em Translation it is that opens the window, to let in the light; that breaks the shell, 
	that we may eat the kernel; that puts aside the curtain, that we may look into the most holy place; 
	that removes the cover of the well, that we may come by the water.\em* (“The Translators to the 
	Reader,” King James Version, 1611).
	\im The most important document in the history of the English language is the \bk King James 
	Version\bk* of the Bible...

.. image:: images/usfm-paragraph_im.jpg
	:width: 250px

-----

.. _usfmp_imi:
.. index:: marker; \imi, introductions; indented margin paragraph

\\imi
^^^^^

:Syntax: ``\imi_text...``
:Type: paragraph
:Added: 1.0
:Use: Indented introduction flush left (margin) paragraph. |br|

**Text and Formatting Sample** - Introduction to the GCEV

.. code-block:: text
	:name: usfm-paragraph_imi_example
	:emphasize-lines: 3

	\imt1 Preface:
	\is1 A Word about the Contemporary English Version
	\imi \em Translation it is that opens the window, to let in the light; that breaks the shell, 
	that we may eat the kernel; that puts aside the curtain, that we may look into the most holy place; 
	that removes the cover of the well, that we may come by the water.\em* (“The Translators to the 
	Reader,” King James Version, 1611).
	\im The most important document in the history of the English language is the \bk King James 
	Version\bk* of the Bible...

.. image:: images/usfm-paragraph_imi.jpg
	:width: 250px

-----

.. _usfmp_ipq:
.. index:: marker; \ipq, introductions; text quote paragraph

\\ipq
^^^^^

:Syntax: ``\ipq_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction quote from text paragraph. |br|

**Text and Formatting Sample** - Introduction to Genesis (CEV)

.. code-block:: text
	:name: usfm-paragraph_ipq_example
	:emphasize-lines: 4

	... One of these brothers, Joseph, had become the governor of Egypt. But Joseph knew that 
	God would someday keep his promise to his people:
	\ib
	\ipq Before Joseph died, he told his brothers, “I won't live much longer. But God will take 
	care of you and lead you out of Egypt to the land he promised Abraham, Isaac, and Jacob.”
	\ipr (50.24)
	\iot A QUICK LOOK AT THIS BOOK
	...

.. image:: images/usfm-paragraph_ipq.jpg
	:width: 450px

-----

.. _usfmp_imq:
.. index:: marker; \imq, introductions; margin text quote paragraph

\\imq
^^^^^

:Syntax: ``\imq_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction flush left (margin) quote from text paragraph. |br|

**Text and Formatting Sample** - Introduction to Genesis (CEV)

.. code-block:: text
	:name: usfm-paragraph_imq_example
	:emphasize-lines: 4

	... One of these brothers, Joseph, had become the governor of Egypt. But Joseph knew that 
	God would someday keep his promise to his people:
	\ib
	\imq Before Joseph died, he told his brothers, “I won't live much longer. But God will take 
	care of you and lead you out of Egypt to the land he promised Abraham, Isaac, and Jacob.”
	\ipr (50.24)
	\iot A QUICK LOOK AT THIS BOOK
	...

.. image:: images/usfm-paragraph_imq.jpg
	:width: 450px

-----

.. _usfmp_ipr:
.. index:: marker; \ipr, introductions; right-aligned paragraph

\\ipr
^^^^^

:Syntax: ``\ipr_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction right-aligned paragraph. |br|
	Typically used for a quote from text reference. |br|

**Text and Formatting Sample** - Introduction to Genesis (CEV)

.. code-block:: text
	:name: usfm-paragraph_ipr_example
	:emphasize-lines: 6

	... One of these brothers, Joseph, had become the governor of Egypt. But Joseph knew that 
	God would someday keep his promise to his people:
	\ib
	\ipq Before Joseph died, he told his brothers, “I won't live much longer. But God will take 
	care of you and lead you out of Egypt to the land he promised Abraham, Isaac, and Jacob.”
	\ipr (50.24)
	\iot A QUICK LOOK AT THIS BOOK
	...

.. image:: images/usfm-paragraph_ipr.jpg
	:width: 250px

-----

.. _usfmp_iq#:
.. index:: marker; \iq#, introductions; poetic line

\\iq#
^^^^^

:Syntax: ``\iq#_text...``
:Type: paragraph
:Added: 1.0
:Use: 	Introduction poetic line. |br|
	The variable # represents the indent level (i.e. \iq1, \iq2, \iq3 etc.) |br|
	**\\iq = \\iq1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Sample** - Introduction to Titus (CEV)

.. code-block:: text
	:name: usfm-paragraph_iq#_example
	:emphasize-lines: 3-9

	\ip Paul also tells how we are saved:
	\ib
	\iq1 God our Savior showed us
	\iq2 how good and kind he is.
	\iq1 He saved us because
	\iq2 of his mercy,
	\iq1 and not because
	\iq2 of any good things
	\iq2 that we have done.
	\ipr (3.4,5a)

.. image:: images/usfm-paragraph_iq.jpg
	:width: 250px

-----

.. _usfmp_ib:
.. index:: marker; \ib, introductions; blank line

\\ib
^^^^

:Syntax: ``\ib``
:Type: paragraph
:Added: 1.0
:Use: Introduction blank line. |br|
	May be used to explicitly indicate additional white space between paragraphs.

**Text and Formatting Sample** - Introduction to Genesis (CEV)

.. code-block:: text
	:name: usfm-paragraph_ib_example
	:emphasize-lines: 3

	... One of these brothers, Joseph, had become the governor of Egypt. But Joseph knew that 
	God would someday keep his promise to his people:
	\ib
	\imq Before Joseph died, he told his brothers, “I won't live much longer. But God will take 
	care of you and lead you out of Egypt to the land he promised Abraham, Isaac, and Jacob.”

|ico_See| *See also* :ref:`\\ipq <usfmp_ipq>`, :ref:`\\imq <usfmp_ib>` examples (above).

-----

.. _usfmp_ili#:
.. index:: marker; \ili#, introductions; list item

\\ili#
^^^^^^

:Syntax: ``\ili#_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction list item. |br|
	The variable # represents the level of indent. |br|
	**\\ili = \\ili1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Sample** - Introduction to Mark (Good News Study Bible)

.. code-block:: text
	:name: usfm-paragraph_ili#_example
	:emphasize-lines: 4,11,14

	\ip However, he is more than a teacher, healer, or \w miracle\w*-worker. He is also the 
	Messiah, the Son of God, the Son of Man. These three titles express the first Christians' 
	understanding of who Jesus is.
	\ili 1 \k The Messiah\k* is the one promised by God, the one who would come and free God's 
	people. By the time \bk The Gospel of Mark\bk* appeared, the title "Messiah" (in Greek, 
	"\w christ\w*") had become a proper name, so that the Gospel opens with "the Good News about 
	Jesus Christ" (and not "Jesus the Christ"). Peter's confession (8.29) marks a turning-point 
	in the ministry of Jesus. The title "\w son of  david\w* " (10.46-48) also identifies Jesus 
	as the Messiah, who would restore to Israel the power and glory it enjoyed under David's 
	reign (also 12.35-37).
	\ili 2 \k The Son of God\k* is the title by which the heavenly voice addresses Jesus at his 
	baptism (1.11) and his transfiguration (9.7). And at Jesus' death the Roman officer confesses 
	that Jesus is the Son of God (15.39).
	\ili 3 \k The Son of Man\k* is the title most often used of Jesus, and it appears only on the 
	lips of Jesus. This enigmatic title appears in \bk The Book of Daniel\bk* (Dan 7.13n), where 
	it is applied to the exalted figure to whom God gives universal dominion. In \bk Mark\bk* the 
	title is used of Jesus in three ways: the Son of Man acts with divine power (2.10, 28); he will 
	be rejected, will suffer and die (8.31; 9.9, 12, 31; 10.33-34, 45; 14.21, 41); he will return 
	in power and glory (8.38; 13.26; 14.62).

.. image:: images/usfm-paragraph_ili.jpg
	:width: 300px

-----

.. _usfmp_iot:
.. index:: marker; \iot, introductions; outline title

\\iot
^^^^^

:Syntax: ``\iot_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction outline title. |br|

.. _usfmp_io#:
.. index:: marker; \io#, introductions; outline entry

\\io#
^^^^^

:Syntax: ``\io#_text...(references range)``
:Type: paragraph
:Added: 1.0
:Use: Introduction outline entry. |br|
	The outline entry typically ends with a range of references in parentheses. References may be marked with :ref:`\\ior ...\\ior* <usfmc_ior>`. |br|
	The variable # represents the outline (indent) level. |br|
	**\\io = \\io1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Sample** - Introduction to Mark (CEV)

.. code-block:: text
	:name: usfm-paragraph_io#_example
	:emphasize-lines: 3-9

	\ip The two endings to the Gospel, which are enclosed in brackets, are generally regarded 
	as written by someone other than the author of \bk Mark\bk*
	\iot Outline of Contents
	\io1 The beginning of the gospel (1.1-13)
	\io1 Jesus' public ministry in Galilee (1.14–9.50)
	\io1 From Galilee to Jerusalem (10.1-52)
	\io1 The last week in and near Jerusalem (11.1–15.47)
	\io1 The resurrection of Jesus (16.1-8)
	\io1 The appearances and ascension of the risen Lord (16.9-20)
	\c 1
	\s The Preaching of John the Baptist
	\r (Matthew 3.1-12; Luke 3.1-18; John 1.19-28)
	\p
	\v 1 This is the Good News about Jesus Christ

.. image:: images/usfm-paragraph_io.jpg
	:width: 350px

-----

.. _usfmc_ior:
.. index:: marker; \ior ...\ior*, introductions; outline reference range

\\ior ...\\ior\*
^^^^^^^^^^^^^^^^

:Syntax: ``\ior_text...\ior*``
:Type: character
:Added: 1.0
:Use: Introduction outline reference range. |br|
	An outline entry typically ends with a range of references in parentheses. This is an optional character style for marking (and potentially formatting) these references separately. |br|

**Text and Formatting Sample** - Introduction to Mark (CEV)

.. code-block:: text
	:name: usfm-character_ior_example
	:emphasize-lines: 1-6

	\io1 The beginning of the gospel \ior (1.1-13)\ior*
	\io1 Jesus' public ministry in Galilee \ior (1.14–9.50)\ior*
	\io1 From Galilee to Jerusalem \ior (10.1-52)\ior*
	\io1 The last week in and near Jerusalem \ior (11.1–15.47)\ior*
	\io1 The resurrection of Jesus \ior (16.1-8)\ior*
	\io1 The appearances and ascension of the risen Lord \ior (16.9-20)\ior*

.. image:: images/usfm-character_ior.jpg
	:width: 350px

-----

.. _usfmc_iqt:
.. index:: marker; \iqt ...\iqt*, introductions; quoted text

\\iqt ...\\iqt\*
^^^^^^^^^^^^^^^^

:Syntax: ``\iqt_text...\iqt*``
:Type: character
:Added: 2.2
:Use: Introduction quoted text. |br|
	Scripture quotations, or other quoted text, appearing in the introduction.

-----

.. _usfmp_iex:
.. index:: marker; \iex, identification; bridge text, introduction; bridge text

\\iex
^^^^^

:Syntax: ``\iex_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction explanatory or bridge text. |br| |br|
	|ico_Cg| *Recommended use:* is for an explanation of missing book or section in a short Old Testament, or for attribution sentences found at the end of the 14 Pauline Epistles (most often found in hand written texts to identify the author, place of composition but does occur in some printed works).

**Text Sample** - After Romans 16 (KJV54 - BFBS)

.. code-block:: text
	:name: usfm-paragraph_iex_example
	:emphasize-lines: 2

	\v 27 to God only wise, \add be\add* glory through Jesus Christ for ever. Amen.
	\iex Written to the Romans from Corinthus, and sent by Phebe servant of the church at Cenchrea.

-----

.. _usfmp_imte#:
.. index:: marker; \imte#, introductions; major title ending

\\imte#
^^^^^^^

:Syntax: ``\imte#_text...``
:Type: paragraph
:Added: 1.0
:Use: Introduction major title ending. |br|
	Used to mark a major title indicating the end of the introduction. |br|
	The variable # represents a portion of the title, with the lesser emphasis (relative weighting) being on the higher numbers. |br|
	**\\imte = \\imte1** (see :ref:`syntax notes <syntax_numberedMarkers>` on numbered markers)

**Text and Formatting Sample** - Introduction to Mark

.. code-block:: text
	:name: usfm-paragraph_imte#_example
	:emphasize-lines: 1

	\imte End of the Introduction to the Gospel of Mark

-----

.. _usfmp_ie:
.. index:: marker; \ie, introductions; introduction end

\\ie
^^^^^

:Syntax: ``\ie``
:Type: paragraph
:Added: 1.0
:Use: Introduction end. |br|
	Optionally included to explicitly indicate the end of the introduction material.

**Text and Formatting Sample** - Introduction to Mark (GNT)

.. code-block:: text
	:name: usfm-paragraph_??_example
	:emphasize-lines: 3

	\io1 The resurrection of Jesus (16.1-8)
	\io1 The appearances and ascension of the risen Lord (16.9-20)
	\ie
	\c 1
	\s The Preaching of John the Baptist
	\r (Matthew 3.1-12; Luke 3.1-18; John 1.19-28)
	\p
	\v 1 This is the Good News about Jesus Christ
