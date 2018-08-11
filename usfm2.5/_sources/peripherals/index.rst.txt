.. include:: /_static/inc_styles.txt

.. index:: peripherals, peripherals (books), peripherals (divisions), marker (\periph), periph

Peripherals
===========

The following represents a strategy for applying USFM markup to various peripheral content elements which may be prepared for publication in addition to the scripture body text. Peripheral content markup is accomplished through re-purposing the most appropriate existing USFM marker for the current content type.

As with scripture text books, an :ref:`\\id <usfmp_id>` marker is used for identifying the content of the peripheral file. Content should be created in separate book files according to the following general groupings. Within each book, divisions (sub-sections) of content are denoted using the marker ``\periph`` followed by an additional division argument/title. In practice we find that some back matter content is large enough to require storing it in its own book file (Concordance, Glossary, Topical Index, Names Index).

Peripheral Books and Divisions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

+-------------------------------+----------------------------------+------------------------------+
| :doc:`Front Matter <front>`   | :doc:`Introductions <intros>`    | :doc:`BackMatter <back>`     |
| (\\id FRT)                    | (\\id INT)                       | (\\id BAK)                   |
+===============================+==================================+==============================+
| **Divisions**                 | **Divisions**                    | **Divisions**                |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Title Page``        | ``\periph Bible Intorduction``   | ``\periph Chronology Test``  |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Half Title Page``   | ``\periph Old Testament          | ``\periph Weights and        |
|                               | Introduction``                   | Measures``                   |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Promotional Page``  | ``\periph Pentateuch             | ``\periph Map Index``        |
|                               | Introduction``                   |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Imprimatur``        | ``\periph History Introduction`` | ``\periph NT Quotes in LXX`` |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Publication Data``  | ``\periph Poetry Introduction``  | **Additional Back Matter**   |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Foreword``          | ``\periph Prophecy               | Concordance (\\id CNC)       |
|                               | Introduction``                   |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Preface``           | ``\periph Deuterocanon           | Glossary (\id GLO)           |
|                               | Introduction``                   |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Table of Contents`` | ``\periph New Testament          | Topical Index (\id TDX)      |
|                               | Introduction``                   |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Alphabetical        | ``\periph Gospels Introduction`` | Names Index (\id NDX)        |
| Contents``                    |                                  |                              |
+-------------------------------+----------------------------------+------------------------------+
| ``\periph Table of            | ``\periph Epistles               | :doc:`Other <other>`         |
| Abbreviations``               | Introduction``                   |                              |
+-------------------------------+----------------------------------+------------------------------+
|                               | ``\periph Letters Introduction`` | **Divisions**                |
+-------------------------------+----------------------------------+------------------------------+
|                               |                                  | ``\periph Cover``            |
+-------------------------------+----------------------------------+------------------------------+
|                               |                                  | ``\periph Spine``            |
+-------------------------------+----------------------------------+------------------------------+

User defined peripheral content divisions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

As needed, a user may add peripheral content for a division not defined in the list above. The new division should begin with \periph, plus a division argument/title. However, USFM compliant publishing applications should use the list presented here as a reference for content to support.

USFM Markup for Peripherals
^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the following topics there is a recommendation and a brief description of the USFM markers which will be most appropriate for use in each peripheral content division. The recommended markup is sufficient for most projects and should be used as a first option. However, in general, any of the existing USFM standard markers may be used in addition to the recommended markers, if the required content cannot be adequately encoded.

.. toctree::
   :maxdepth: 1

   Front Matter <front>
   Introductions <intros>
   Back Matter <back>
   Other <other>

Any non-standard markers used in these books will need to be added to the stylesheet associated with the project.

Authoring peripheral materials within Paratext
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
ParaTExt includes the named peripheral books FRT, INT, BAK, CNC, GLO, TDX, NDX, and OTH in addition to a set of books named from XXA to XXG. These non-Biblical books appear at the end of a project's list of books, and may be used to author the non-biblical text for Front Matter, Back Matter, Introductions, or any other kind of text which should be stored as part of the translation project.
