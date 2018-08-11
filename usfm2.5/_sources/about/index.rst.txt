.. include:: /_static/inc_styles.txt

.. index:: introduction, about, USFM (about)

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
In general terms, a markup language is a special notation for identifying the components and structure of an electronic document. It combines extra information about the text together with the text itself. The extra information is what is expressed using markup. Markup can also include information about the intended presentation of the text, or instructions for how a software process should handle the text. A good markup system is easily identified as separate from the text itself.
 
Standard Format Markers have been used for many years within the Bible translation community as a method for identifying the unique textual elements which exist within an electronic scripture document. SFMs start with a backslash character ``\`` and end with the next space. Over time many different local "standards" for SFM use were developed, adapted, and used, for supporting the varied requirements of Bible translation and publishing projects around the globe.

.. _about_usfm_history:
.. index:: USFM (history)

History of USFM
---------------
The divergent use of SFMs led to a variety of problems – most notably the challenges associated with sharing text or related text processing tools among entities, departments, or partner organizations. Separate and ongoing maintenance of duplicated tools and procedures, which were required for managing the flow of the text through its life-cycle, became costly and very difficult to support.
 
In March 2002 a working group was established within the `United Bible Societies <http://unitedbiblesocieties.org>`_ with the mandate of "crafting a unified specification for SFM use across 4 UBS areas". Having one SFM standard would provide numerous benefits:
 
* Allow more thought and effort to be put into developing just one set of tools and utilities to be shared by all projects:

    - Tools for text checking and analysis.
    - Tools for developing supporting textual resources such as concordances and indexes.
    - Tools for streamlining the publishing process.

* Eliminate or minimize duplication of effort in providing these tools.
* Allow better sharing of both tools and data.
* Allow Paratext users to use one tested and proven stylesheet.
* Prepare the project for a smoother transition to other markup formats or future technologies.
 
Ideally an SFM standard would have as one of its goals that of marking common scriptural element types, and not formatting (presentation) information. USFM has attempted to unify a long history of SFM type scripture markup implementations, some of which were more or less strict in their tolerance for format-oriented markers. The primary focus in USFM development was on unification, not markup creation. What this means is that USFM inherits support for both the positive, and some negative, aspects of pre-existing SFM marker use. The USFM working group did not wish to create an unmanageable conversion task for legacy SFM encoded texts.

.. _about_usfm_unification:
.. index:: USFM (unification notes)

Unification Notes
-----------------
* Markers which would be used in a broader text "environments" were named using a reserved initial letter, rather than an opening and closing tag:

    - ``\i`` - Introductions
    - ``\f`` - Footnotes
    - ``\x`` - Cross references
    - ``\e`` - Explanatory (study) material - for extended notes, sidebars and bridge materials.

* Related marker types were often consolidated using “numbered” marker definitions.

    - Example: ``\mt#``, ``\ms#``, ``\s#``, ``\li#`` etc., where the variable # represents a number which can indicate a level or relative weighting.

* Marker definition "collisions" were resolved (same marker used to mark different content).

.. _about_usfm_software:
.. index:: USFM (software notes)

Software Notes
--------------

* Translation editors which implement support for USFM encoded text may provide a formatted view of the text using a set of style definitions for each USFM marker. These "stylesheets" most often refer to these formatting definitions as *paragraph* and *character* styles.
* In USFM, character level markup can be nested (embedded) within a paragraph element, or another character element. However, software applications will not necessarily be capable of rendering all of the display variations which may be implied due to marker nesting.

.. _about_usfm_extension:
.. index:: USFM (extension)

Markup Additions/Extensions
---------------------------
Over the course of its development it has become clear that the USFM standard will not likely include and handle markup for all potential (real or perceived) markup needs which a project may require. There are a number of reasons for this, which include:
 
* **The intention of keeping the USFM marker inventory manageable** from a typical end user's perspective. |br| Some may argue that the more than 180 existing marker possibilities are already more than challenging enough to select from and use correctly. For this reason a "draft" stylesheet was created for Paratext editing which lists only the essential markers for editing a typical translation's 1st draft text. |br| |br| 
* **The intention to encourage content oriented markup.** |br| Although USFM contains markers which are format (presentation) oriented (see History of USFM), the use of these is typically discouraged, wherever an suitable alternative is available. |br| |br|
* **The intention to maintain a stable target for tool developers.** |br| The USFM marker inventory cannot continue to evolve and develop indefinitely without minimizing the benefit it potentially offers to developers working on text checking, analysis, conversion, and publishing tools. A stable target is needed for these tools to work against.

Since USFM 1.0, requests for additions to the standard have been received and considered by the USFM committee (see Release Notes for some details). The committee has made a choice to specifically exclude new markers submissions that specify formatting from becoming part of USFM. What this means is that the USFM standard is open to the consideration of new markup needs, but closed to allowing new format oriented markup. At times this position has caused some frustration for users who might otherwise be quite satisfied with USFM, but would be greatly assisted by adding markup to their text which is not a part of the standard.

.. _about_usfm_znamespace:
.. index:: marker (\z ...)

Option: The \\z namespace
-------------------------
As a means of offering a type of solution to the need for occasional local markup additions/extension, USFM recommends that any additional user generated markup should begin with **\\z** (e.g. ``\zMyMarker``). Markers in this namespace will not be considered a part of the USFM standard, or be generally supported in USFM aware applications. This namespace will acts as a type of "private use area". It will be the user or tool builder's responsibility to support support \\z markup in ways which meet a local need. Other USFM processing tools cannot be expected to handle \\z markup or associated text, and are free to ignore them when they are encountered in the text.

.. tip::

	Scripture translation and publishing software `ParaTExt <http://paratext.org/about/pt>`_ and `Publishing Assistant <http://paratext.org/about/pa>`_ both provide a mechanism for adding information about user generated or customized markers to a specific project's configuration. This makes it possible to support proper functioning of checking and formatting tools for the added markup.
 
However, it is much less likely that emerging digital publishing systems and work-flows will support user-generated/non-standardized project markup. Current procedures for interacting with these partner environments requires that translation data is delivered in rigidly validated formats which conform to specific agreed-upon interchange standards, such as the known USFM marker inventory, or some XML-based equivalents. Since connecting with these environments is much more exclusively software-driven than with many print production tools, encountering unknown markup within the publishing processes is a significant problem. Please consider this carefully before introducing non-standard USFM markup within a scripture translation project text.

.. _about_usfm_sty:
.. index:: stylesheets (ParaTExt)

ParaTExt Stylesheets
--------------------
The most recent full and draft USFM stylesheet files for use with the ParaTExt translation editor are always available from http://paratext.org/usfm.
