.. include:: /_static/inc_styles.txt

.. index:: study content; categories, categories

Categories
==========

Categories can optionally be assigned to extended study notes or sidebars by supplying a category tag (name) inside of opening and closing ``\cat ...\cat*`` markers. Category tags should be restricted to alpha-numeric characters. A list of category tags are defined individually and uniquely for each study Bible project.

.. _usfmc_cat:
.. index:: marker; \cat ...\cat*

\\cat ...\\cat\*
----------------

:Syntax: ``\cat_<TAG>\cat*``
:Type: character (extended note)
:Added: 2.1
:Use: Extended note or sidebar category tag.

.. note::

	**Implementations:** The `ParaTExt <http://paratext.org>`_ translation editor provides an interface for supplying a pre-defined content category tag list for a study Bible project. Paratext can use this list to guide the author toward using only categories from the pre-defined set. Support for formatting content with different category tags needs to be provided by the publishing solution in use. The Custom Layout features in `Publishing Assistant <http://pubassist.paratext.org>`_ (>=4.0) provide advanced support for handling study content categories.

-----

.. rubric:: Text and Formatting Samples

**Extended Footnotes with Category Tag** - Matthew 2.4 (Good News Study Bible - UK)

.. code-block:: text
	:name: usfm-character_cat_example-footnote
	:emphasize-lines: 7,9-10

	\p
	\v 1 This is the list of the ancestors of Jesus Christ, a descendant of David, who 
	was a descendant of Abraham.
	\p
	\v 2-6a From Abraham to King David, the following ancestors are listed: Abraham, 
	Isaac, Jacob, Judah and his brothers; then Perez and Zerah (their mother was Tamar
	\ef - \cat People\cat*\fr 1.2-6a: \fq Tamar: \ft Bore her twin sons out of wedlock 
	(Gen 38.6-30).\ef*), Hezron, Ram, Amminadab, Nahshon, Salmon, Boaz (his mother was Rahab
	\ef - \cat People\cat*\fr 1.2-6a: \fq Rahab: \ft A prostitute in Jericho (Josh 2.1-21; 
	6.17-25; Jas 2.25).\ef*), Obed (his mother was Ruth\ef - \cat People\cat*\fr 1.2-6a: 
	\fq Ruth: \ft A Moabite (Ruth 1.4). Only outstanding women were normally included in 
	Jewish genealogical lists.\ef*), Jesse, and King David.
	\p
	\v 6b-11 From David to the time when the people of Israel were taken into exile in 
	Babylon\ef - \fr 1.6b-11: \fq exile in Babylon: \ft In 597 \sc BC\sc* King Nebuchadnezzar 
	of Babylonia conquered Jerusalem and took many of its inhabitants as prisoners to his 
	country (2 Kgs 24.10-16; 2 Chr 36.9-10).\ef*, the following ancestors are listed: ...

.. image:: images/usfm-character_cat-footnote.png
	:width: 350px

**Sidebar with Category Tag** - Matthew 2.4 (CEV Learning Bible)

.. code-block:: text
	:name: usfm-character_cat_example-sidebar
	:emphasize-lines: 4

	\v 4 \ef - \fr 2.4: \fk Chief Priests\ef*\ef - \fr 2.4: \fk Teachers of the Law\ef*He 
	called together all the chief priests and the teachers of the Law and asked them, “Where 
	will the Messiah be born?”
	\esb \cat Ideas\cat*
	\ms Dates in B.C. and A.D.
	\p The initials \sc b.c.\sc* have traditionally been an abbreviation for “Before Christ.” 
	If \bk Luke\bk*'s dating is correct, then Jesus was born at least four years before the 
	years known as \sc a.d.\sc* began. (\sc a.d.\sc* stands for the Latin phrase “in the year 
	of our Lord”). Christian dating was actually not introduced until \sc a.d.\sc* 526 by a 
	monk named Dionysius Exiguus. He was given the job of creating a calendar for the feasts 
	of the church. He fixed the birth of Jesus in the Roman year 754, which was selected as 
	the first year of the Christian era beginning on January 1. Dionysius apparently 
	misjudged Herod's reign by about five years.
	\p The initials \sc b.c.\sc*e. (Before the Common Era) and c.e. (in the Common Era) are 
	sometimes used for the traditional \sc b.c.\sc* and \sc a.d.\sc*
	\esbe
	\p
	\v 5 \ef - \fr 2.5: \fk Prophet\ef*“In the town of Bethlehem in Judea,” they answered. 
	“For this is what the prophet wrote:

*Example 1: Category based formatting using background colors*

.. image:: images/usfm-character_cat-sidebar1.png
	:width: 550px


*Example 2: Category based formatting using images/icons*

.. image:: images/usfm-character_cat-sidebar2.png
	:width: 550px
