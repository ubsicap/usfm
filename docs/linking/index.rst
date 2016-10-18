.. include:: /_static/inc_styles.txt

.. index:: linking
	pair: attributes; linking

Linking Attributes
==================

|badge_3.0|

Following the :ref:`general syntax <attributes_syntax>` for :doc:`word level attributes </attributes/index>`, USFM 3.0 provides a set of attributes for assigning linking properties to character level elements.

General Syntax
^^^^^^^^^^^^^^

Names given to linking attributes begin with ``link-``, distinguishing them from any other descriptive :ref:`attributes <attributes_markersProviding>`. Linking attributes are separated from the text content by a vertical bar ``|``. Attributes are listed as pairs of name and corresponding value using the syntax: ``link-<attribute> = "value"``.

Linking attributes are combined with any other descriptive attributes added to the same marker. The order of attributes is not significant, although it would benefit readability to have descriptive and linking attributes grouped together.

Attributes
^^^^^^^^^^

* **link-href** - identifies the resource being linked to as a URI.

    - Custom USFM provided URI prefixes are:

        + ``prj:`` + standard USFM / USX scripture reference syntax (book, chapter, verse). Example: ``prj:RSV52 MAT 3:1-4``

    - A link reference within the same project text does not require a URI prefix but must follow the standard USFM / USX scripture reference syntax. Example: ``MAT 3:1-4``
    - The resource may be identified by unique id. Example: ``#article-Ruth`` or ``prj:GNTSB #article-Ruth``

* **link-title** - plain text describing the remote resource such as might be shown in a tooltip.
* **link-name** - a unique identifier for this content location (an anchor).

The set of URI prefixes used within a ``link-href`` attribute can be extended beyond the predefined set for USFM 3.0. Any user defined URI prefixes must begin with the prefix ``x-``.

**Examples:**

Link to other project text

.. code-block:: text
	:emphasize-lines: 2

	The traditional translation of verse 1, as given in 
	\jmp RSV|link-href="prj:RSV52 GEN 1:1" link-title="Revised Standard Version"\jmp*, 
	may be appropriate.

Link to illustration / media

.. code-block:: text
	:emphasize-lines: 2-3

	Storehouses, as used here, refers to large buildings with walls and roof, where grain was 
	kept until needed. (See illustration: \jmp Storehouse|link-href="figures/storehouse.png" 
	link-title="Ancient storehouse"\jmp*)

Assigning an identifier (anchor). *In this example the markup is a milestone, indicating a location but not marking text.*

.. code-block:: text
	:emphasize-lines: 5

	\q1 “Someone is shouting in the desert,
	\q2 ‘Prepare a road for the Lord;
	\q2 make a straight path for him to travel!’ ”
	\esb \cat People\cat*
	\ms \jmp |link-name="article-john_the_baptist"\jmp*John the Baptist
	\p John is sometimes called the last “Old Testament prophet” because of the warnings he 
	brought about God's judgment and because he announced the coming of God's “Chosen 
	One” (Messiah).

Glossary entry including a link reference to an external URL

.. code-block:: text

	\w gracious|link-href="http://bibles.org/search/grace/eng-GNTD/all"\w*

Reference to named target within the same project

.. code-block:: text
	:emphasize-lines: 4

	\p \v 2-6a From Abraham to King David, the following ancestors are listed: Abraham, 
	Isaac, Jacob, Judah and his brothers; then Perez and Zerah (their mother was Tamar*), 
	Hezron, Ram, Amminadab, Nahshon, Salmon, Boaz (his mother was Rahab*), Obed (his 
	mother was \jmp Ruth|link-href="#article-Ruth"\jmp*), Jesse, and King David. 

:doc:`Nested </characters/nesting>` markup (within :doc:`extended footnote </notes_study/efnotes>`)

.. code-block:: text
	:emphasize-lines: 3

	\ef - \fr 1.2-6a: \fq Ruth: \ft A Moabite (Ruth 1.4). Only outstanding 
	women were normally included in Jewish genealogical lists. See article 
	on \+jmp Ruth|link-href="#article-Ruth"\+jmp*\ef*

-----

.. _usfmc_jmp:
.. index:: marker; \jmp ...\jmp*

\\jmp ...\\jmp\*
^^^^^^^^^^^^^^^^

|badge_3.0|

:Syntax: ``\jmp text...|link-href="..."\jmp*``
:Type: character
:Added: 3.0
:Use: Link text. |br|
	Optionally used for associating linking attributes to a span of text when no other character level markup is applied to the same span.

*Linking examples provided above*
