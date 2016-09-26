.. include:: /_static/inc_styles.txt

.. index:: milestones, speaker; start/end markup

Milestones
==========

|badge_3.0|

USFM 3.0 provides a general syntax for indicating the start and ending milestones for a span of text, where the boundaries of the content being marked may cross one or more paragraph boundaries.

A milestone type markup is required when a document has two or more structures that interact in a non-hierarchical manner. This is also referred to as *overlapping* or *concurrent* markup. A principle example of this type of overlapping structure in scripture text is the contrast between 1) the paragraph structures used to express the discourse / narrative of the text and 2) the division of the text into books, chapters and verses. In scripture texts encoded using USFM (and similarly also in `USX <https://ubsicap.github.io/usx/index.html>`_), the paragraph level markup forms the main structure of the document, while :ref:`chapter <usfmp_c>` and :ref:`verse <usfmc_v>` markers are effectively a milestone type.

Another example of an overlapping structure exists when there is a need to indicate the start and end of the quotations of the "actors" who are speaking within the text. These spans of text will commonly cross paragraph boundaries.

.. _milestones_syntax:
.. index:: miletones; syntax

General Syntax
^^^^^^^^^^^^^^

Milestones follow a syntax similar to the current :doc:`character level markup </characters/index>`. The significant distinguishing feature is that milestones introduce a new **self-closing** syntax. This self-closing syntax is the feature which identifies the marker as a milestone. The milestone will mark the *position* of the start or end of a span of text, but it does not strictly *contain* the text, as with a regular character level markup.

A benefit of the self-closing marker syntax is that it also results in a shorter marker string.

Self closing markup is indicated by immediately terminating the marker, and any attributes, with a backslash plus asterisk.

**Example:** (milestone for the start of a quotation / speaker)

.. code-block:: text

    \qts\*

.. _milestones_startend:
.. index:: miletones; start and end

Indicating Start and End Milestones
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A milestone marker must always end with either ``s`` or ``e``

* ``s`` indicates that the milestone is for marking the **start** of a span of text.
* ``e`` indicates that the marker is an **end** milestone.

**Example:** (milestone for the end of a quotation / speaker)

.. code-block:: text

    \qte\*

.. _milestones_attributes:
.. index:: milestones; attributes

Attributes
^^^^^^^^^^

Following the syntax for :doc:`word level attributes </attributes/index>`, the following optional attributes can be added to *any* USFM milestone marker.

:id: A unique identifier which can be used to unambiguously associate the start and ending milestone marker. |br|
	The id can be composed of any mixture of numbers, letters, and underscores, and should be unique throughout the scripture text for the selected milestone type.

**Example:**

.. code-block:: text

    \qts |id="123" who="Pilate"\*“Are you the king of the Jews?”\qte |id="123"\*

Additional attributes may be available for or required by a specific USFM milestone marker (e.g the use of the ``who`` attribute in the above :ref:`quotation milestone <usfmm_qt#s>` example).

Levels
^^^^^^

As with other USFM :ref:`numbered markers <syntax_numberedMarkers>`, a numeric variable may be added to a milestone marker to indicate a relative weighting or level. In the example of the quotation / speaker milestone, a numbered version of the marker may be used to indicate the level of nesting of the quotation being marked (i.e. a quote within a quote).

The unnumbered version may be used when only one level of marker exists within the project text. Numbers should always be included when more than one level of the marker exists within the project text.

-----

.. _usfmm_qt#s:
.. index:: marker; \qt#s\*, marker; \qt#e\*, milestone; \qt#s\*, milestone; \qt1e\* 

\\qt#s\\*
^^^^^^^^^