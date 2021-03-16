.. include:: /_static/inc_styles.txt

.. index:: introduction
  pair: USFM; about

************
Introduction
************

.. toctree::
   :maxdepth: 1

   Release Notes <releasenotes>
   Syntax Notes <syntax>

-----

.. _about_sfm:
.. index:: SFM, marker

What are Standard Format Markers?
---------------------------------
A markup language is a special notation for identifying the components and structure of an electronic document. It combines meta information about the text together with the text itself. The meta information is what is expressed using markup. Markup can also include information about the intended presentation of the text, or instructions for how a software process should handle the text. A good markup system is easily identified as separate from the text itself.
 
Standard Format Markers (SFMs) have been used for many years within the Bible translation community as a method for identifying the unique textual elements within a digital scripture text. Generally, SFMs start with a backslash character ``\`` and end with the next space. Over years many different local "standards" for SFM use were developed, adapted, and used for supporting the varied requirements of Bible translation and publishing projects in different areas of the world.

.. _about_usfm_history:
.. index:: pair: USFM; history

History of USFM
---------------
The diverging use of SFMs led to various problems – most notably the challenge associated with sharing text or text processing tools between organization departments or with partnering organizations. Maintenance of software tools and procedures for handling texts using differing collections of SFMs became costly and difficult to support.
 
In March 2002 a working group was established within the `United Bible Societies <http://unitedbiblesocieties.org>`_ with the mandate of producing a unified specification for SFM use across 4 UBS areas.
 
Ideally an SFM standard would seek to identify and mark all common scriptural element types, and avoid markup primarily for formatting (presentation) information. USFM has attempted to unify a long history of SFM scripture markup implementations, some of which were more or less strict in their tolerance for format-oriented markers. USFM development focused primarily on unification, not new markup creation. Practically speaking, this means is that USFM inherits support for both the positive, and some negative, aspects of pre-existing SFM marker use.

.. _about_usfm_unification:
.. index:: USFM; unification notes

Unification Notes
-----------------
* Markers which would be used in specific text "environments" are named using a reserved initial letter:

    - ``\i`` - Introductions
    - ``\f`` - Footnotes
    - ``\x`` - Cross references
    - ``\e`` - Explanatory (study) material - for extended notes, sidebars and bridge materials.

* Related marker types were usually consolidated using “numbered” marker definitions.

    - Example: ``\mt#``, ``\ms#``, ``\s#``, ``\li#`` etc., where the variable # represents a number which can indicate a level or relative weighting.

* Marker definition "collisions" were resolved (same marker used to mark different content).

.. _about_usfm_software:
.. index:: USFM; software notes

Software Notes
--------------

* Translation editors which implement support for USFM encoded text may provide a formatted view of the text using a set of style definitions for each USFM marker. These "stylesheets" typically refer to these formatting definitions as *paragraph* and *character* styles.
* In USFM, character level markup exists within a paragraph element, or can be :doc:`nested </characters/nesting>` (embedded) within another character element. Software applications will not necessarily be capable of rendering all of the display variations which may be implied due to marker nesting.

.. _about_usfm_changes:
.. index:: USFM; change management

Change Management
-----------------
The USFM standard will not necessarily include markup for all potential (real or perceived) markup needs which a project may require. There are a number of reasons for this, including:
 
* The intent to keep the size of the USFM marker inventory manageable.
* The intention to encourage content oriented markup. |br| Although USFM contains some markers which are format (presentation) oriented (see History of USFM), the use of these is typically discouraged, wherever an suitable alternative is available.
* The intention to maintain a stable target for tool developers.

Since USFM 1.0, requests for additions to the standard have been received and considered by a USFM maintenance committee (see :doc:`Release Notes </about/releasenotes>` for some details).

|ico_See| See also: User extension :ref:`\\z namespace <syntax_znamespace>`.

.. _about_usfm_sty:
.. index:: pair: stylesheet; Paratext

Paratext Stylesheet
-------------------
The most recent USFM stylesheet file for use with the Paratext translation editor are always available from http://markups.paratext.org/usfm, or directly from the USFM Github repository at https://github.com/ubsicap/usfm/tree/master/sty.
