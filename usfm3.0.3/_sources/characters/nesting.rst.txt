.. include:: /_static/inc_styles.txt

.. index:: character marker nesting, marker nesting, nesting

Character Marker Nesting
========================

In USFM, character level markup is applied to text within a containing :doc:`paragraph </paragraphs/index>` element like :ref:`\\p <usfmp_p>` or :ref:`\\q1 <usfmp_q#>`. :doc:`Footnotes </notes_basic/fnotes>` and :doc:`cross references </notes_basic/xrefs>` are marked using a containing element pair like ``\f ...\f*`` or ``\x ...\x*``. The USFM markup used within note elements (like :ref:`\\fq <usfmc_fq>` or :ref:`\\ft <usfmc_ft>` etc.) are also a type of character level marker.

In some scripture translation texts, the USFM markup required to properly mark the types of content within the text will result in one character level marker being “nested” within another character level marker. In this situation it is critical that the editing and publishing environments used for working with the text understand how to interpret, present, and validate the nested markup contexts. Normally, in Paratext, the start of a new character level marker environment is also recognized by the program as an implicit closure of the the previous character environment. When a nested character markup is actually intended, the meaning and formatting applied to the outer layer of the nested markup context should also apply to the inner level(s). The inner markup communicates an additional meaning and formatting for the nested text.

Perhaps the most common occurrence for nested character markup is within footnotes, where some text occurring within a footnote quotation (:ref:`\\fq <usfmc_fq>`), keywords (:ref:`\\fk <usfmc_fk>`), or footnote text itself (:ref:`\\ft <usfmc_ft>`), needs to be marked further.

USFM 2.4 adds a new syntax for indicating that a nesting of one character level marker within another is taking place within a text. Full support for the nested markup syntax has been included in ParaTExt >=7.4, Publishing Assistant >=4.1, and the XML export format from ParaTExt known as `USX <http://markups.paratext.org/usx>`_.

Indicating that a character marker is nested
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When a character level marker is used to mark text already inside of an existing character level environment, a plus sign ``+`` should be used as a prefix to the opening and closing forms of the new nested marker. The ``+`` is added after the backslash, and before the marker text. The ``+`` indicates that a new character environment has started, without closing the previous one.

In the following example text:

* ``\+nd`` indicates to start a new character environment nested inside the existing ``\add`` environment (without closing ``\add``)
* ``\+nd*`` indicates to end the nested environment without closing ``\add``

.. code-block:: text

	The following is a \add translator's addition containing the word \+nd Lord\+nd* 
	within it\add*

All new character marker starts (without the ``+`` prefix) close all existing nesting. The next two examples are both valid nested character markup.

.. code-block:: text

	\p ... \add an addition containing the word \+nd Lord\+nd*\add* and further text ...

	\p ... \add an addition containing the word \+nd Lord\add* and further text ...

If necessary, multiple levels of nesting character markup can occur.

.. note::

	A `ParaTExt <http://paratext.org>`_ project’s project stylesheet(s) will not contain definitions for the nested markers containing ``+``.

**Text and Formatting Sample** - Numbers 21.14 (GNT) - \\bk \\+nd nested

.. code-block:: text
	:name: usfm-character_bk+nd_example
	:emphasize-lines: 1

	\v 14 That is why \bk The Book of the \+nd Lord\+nd*'s Battles\bk* speaks of “...the 
	town of Waheb in the area of Suphah, and the valleys; the Arnon River,
	\v 15 and the slope of the valleys that extend to the town of Ar and toward the border 
	of Moab.”

.. image:: images/usfm-character_bknd-nested.jpg
	:width: 250px

Genesis 2.4 (GNT) - \\fk \\+nd nested

.. code-block:: text
	:name: usfm-character_fk+nd_example
	:emphasize-lines: 1

	\s1 The Garden of Eden
	\p When the \nd Lord\nd* \f + \fr 2.4: \fk the \+nd Lord\+nd*: \ft Where the Hebrew text 
	has Yahweh, traditionally transliterated as Jehovah, this translation employs \+nd Lord\+nd* 
	with capital letters, following a usage which is widespread in English versions.\f* God made 
	the universe,
	\v 5 there were no plants on the earth and no seeds had sprouted, because he had not sent 
	any rain, and there was no one to cultivate the land;

.. image:: images/usfm-character_fknd-nested.jpg
	:width: 550px
