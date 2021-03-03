.. include:: /_static/inc_styles.txt

.. index:: chapters, verses

Chapters and Verses
===================

.. _usfmp_c:
.. index:: marker; \c, chapters; chapter number

\\c
^^^

:Syntax: ``\c_#``
:Type: paragraph
:Added: 1.0
:Use: Chapter number. |br|
	The marker is followed by the chapter number #. |br|
	No further text should follow this marker.

**Text and Formatting Sample** - Matthew 1 (GNT)

.. code-block:: text
	:name: usfm-paragraph_c_example
	:emphasize-lines: 3

	\io1 The last week in and near Jerusalem (21.1–27.66)
	\io1 The resurrection and appearances of the Lord (28.1-20)
	\c 1
	\s1 The Ancestors of Jesus Christ
	\r (Luke 3.23-38)
	\p
	\v 1 This is the list of the ancestors of Jesus Christ, a descendant of David, who was a 
	descendant of Abraham.

.. image:: images/usfm-paragraph_c.jpg
	:width: 250px

-----

.. _usfmc_ca:
.. index:: marker; \ca ...\ca*, chapters; alternate chapter number

\\ca ...\\ca\*
^^^^^^^^^^^^^^

:Syntax: ``\ca_#\ca*``
:Type: character
:Added: 1.0
:Use: Alternate chapter number. |br|
	Used for marking the chapter number used in an alternate versification scheme. Required when different versification traditions need to be supported in the same translation text. |br|
	The content within the marker pair should only contain the alternate chapter number, and not include any formatting/

**Text and Formatting Sample** - Psalm 54 (GNT - *markup adapted*)

.. code-block:: text
	:name: usfm-character_ca_example
	:emphasize-lines: 2

	\c 54
	\ca 53\ca*
	\s1 A Prayer for Protection from Enemies
	\d \va 1\va* A poem by David, \va 2\va* after the men from Ziph went to Saul and told him 
	that David was hiding in their territory.
	\q1
	\v 1 \va 3\va* Save me by your power, O God;
	\q2 set me free by your might!
	\q1
	\v 2 \va 4\va* Hear my prayer, O God;
	\q2 listen to my words!

.. image:: images/usfm-character_ca.jpg
	:width: 250px

-----

.. _usfmp_cl:
.. index:: marker; \cl, chapters; chapter label

\\cl
^^^^

:Syntax: ``\cl_text...``
:Type: paragraph
:Added: 1.0
:Use: The chapter "label" to be used when the chosen publishing presentation will render chapter divisions as headings (not drop cap numerals).

.. note::

	**Usage note:** If \\cl is entered once before chapter 1 (\\c 1) it represents the text for "chapter" to be used throughout the current book. If \\cl is used after each individual chapter marker, it represents the particular text to be used for the display of the current chapter heading (usually done if numbers are being presented as words, not numerals).

**Text and Formatting Samples** - Psalm 1 (GNT - *markup adapted* - general chapter label)

.. code-block:: text
	:name: usfm-paragraph_cl_example
	:emphasize-lines: 1

	\cl Psalm
	\c 1
	\q1 
	\v 1 Happy are those 
	\q2 who reject the advice of evil people,

.. image:: images/usfm-paragraph_cl.jpg
	:width: 250px

Psalm 1 (GNT - *markup adapted* - specific chapter label)

.. code-block:: text
	:name: usfm-paragraph_cl_example-alt
	:emphasize-lines: 2

	\c 1
	\cl Psalm One
	\q1 
	\v 1 Happy are those 
	\q2 who reject the advice of evil people,

.. image:: images/usfm-paragraph_cl-alt.jpg
	:width: 250px

-----

.. _usfmp_cp:
.. index:: marker; \cp, chapters; published chapter character

\\cp
^^^^

:Syntax: ``\cp_text...``
:Type: paragraph
:Added: 1.0
:Use: Published chapter character. |br|
	This is the chapter character (number, letter) which should be displayed in the published text (where the published marker is different than the :ref:`\\c # <usfmp_c>` used within the translation editing environment).

**Text and Formatting Sample** - Esther-Greek 1 ("A") (GNT)

.. code-block:: text
	:name: usfm-paragraph_cp_example
	:emphasize-lines: 2

	\c 1
	\cp A
	\s1 Mordecai's Strange Dream
	\p
	\v 1-3 \va 2-4\va* Mordecai, a Jew who belonged to the tribe of Benjamin, was taken into 
	exile, along with King Jehoiachin of Judah, when King Nebuchadnezzar of Babylonia captured 
	Jerusalem. ...

.. image:: images/usfm-paragraph_cp.jpg
	:width: 250px

-----

.. _usfmp_cd:
.. index:: marker; \cd; chapters; chapter description

\\cd
^^^^

:Syntax: ``\cd_text...``
:Type: paragraph
:Added: 1.0
:Use: Chapter description. |br|
	A brief description of chapter content (similar to :ref:`\\d <usfmp_d>` - descriptive heading, or :ref:`\\iex <usfmp_iex>` - explanatory or bridge text).

**Text and Formatting Sample** - Genesis 2 (Russian Synodal, Protestant Version)

.. code-block:: text
	:name: usfm-paragraph_cd_example
	:emphasize-lines: 2

	\c 2
	\cd 1 Бог благословляет седьмой день; 8 человек в раю Едемском; четыре реки; дерево 
	познания добра и зла. 18 Человек дает названия животным. 21 Создание женщины.
	\p
	\v 1 Так совершены небо и земля и все воинство их.
	\p
	\v 2 И совершил Бог к седьмому дню дела Свои, которые Он делал, и почил в день седьмой 
	от всех дел Своих, которые делал.

.. image:: images/usfm-paragraph_cd.jpg
	:width: 250px

-----

.. _usfmc_v:
.. index:: marker; \v, verses; verse number

\\v
^^^

:Syntax: ``\v_#_``
:Type: character
:Added: 1.0
:Use: Verse number. |br|
	The marker is followed by the verse number #, then a space (which marks the end of the verse), and then text of the verse.

**Text and Formatting Sample** - Matthew 1.18,19 (GNT)

.. code-block:: text
	:name: usfm-character_v_example
	:emphasize-lines: 4,7

	\s1 The Birth of Jesus Christ
	\r (Luke 2.1-7)
	\p
	\v 18 This was how the birth of Jesus Christ took place. His mother Mary was engaged 
	to Joseph, but before they were married, she found out that she was going to have a 
	baby by the Holy Spirit.
	\v 19 Joseph was a man who always did what was right, but he did not want to disgrace 
	Mary publicly; so he made plans to break the engagement privately.

.. image:: images/usfm-character_v.jpg
	:width: 250px

-----

.. _usfmc_va:
.. index:: marker; \va ...\va*, verses; alternate verse number

\\va ...\\va\*
^^^^^^^^^^^^^^

:Syntax: ``\va_#\va*``
:Type: character
:Added: 1.0
:Use: Alternate verse number. |br|
	Used for marking verse numbers used in an alternate versification scheme. Required when different versification traditions need to be supported in the same translation text. |br|
	The content within the marker pair should only contain the alternate verse number, and not include any formatting/presentation characters (e.g. brackets or parentheses) 

**Text and Formatting Sample** - Psalm 54 (GNT - *markup adapted*)

.. code-block:: text
	:name: usfm-character_va_example
	:emphasize-lines: 4,7,10

	\c 54
	\ca 53\ca*
	\s1 A Prayer for Protection from Enemies
	\d \va 1\va* A poem by David, \va 2\va* after the men from Ziph went to Saul and told 
	him that David was hiding in their territory.
	\q1
	\v 1 \va 3\va* Save me by your power, O God;
	\q2 set me free by your might!
	\q1
	\v 2 \va 4\va* Hear my prayer, O God;
	\q2 listen to my words!

.. image:: images/usfm-character_va.jpg
	:width: 250px

-----

.. _usfmc_vp:
.. index:: marker; \vp ...\vp*, verses; published verse character

\\vp ...\\vp\*
^^^^^^^^^^^^^^

:Syntax: ``\vp text...\vp*``
:Type: character
:Added: 1.0
:Use: Published verse character. |br|
	This is the verse character (number, letter) which should be displayed in the published text (where the published character(s) are different than the :ref:`\\v # <usfmc_v>` digit used within the translation editing environment).

**Text and Formatting Sample** - Esther-Greek 3.14,15 ("Addition B") (CEV)

.. code-block:: text
	:name: usfm-character_vp_example
	:emphasize-lines: 5,9

	\cp 13
	\ms1 Addition B
	\s A Copy of the Letter
	\p
	\v 14 \vp 1b\vp* This is a copy of the letter:
	\pmo From Artaxerxes, the Great King, to the governors and officials of my one hundred 
	twenty-seven provinces from India to Ethiopia.
	\pm
	\v 15 \vp 2b\vp* I rule many nations, and I am the most powerful king in the world. 
	But I have never used my power in a proud or arrogant way. Instead, I have always 
	been reasonable and kind to the people in my kingdom. I know they want peace, and so 
	I have decided to make every part of my kingdom peaceful and safe for travel.

.. image:: images/usfm-character_vp.jpg
	:width: 250px
