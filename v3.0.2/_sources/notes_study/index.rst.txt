.. include:: /_static/inc_styles.txt

.. index:: study content, note; study

Extended Study Content
======================

A study Bible project text is based on an existing scripture translation text. It may be referred to as a "derived text". Typically one or more of the following study content types are added to the text. To distinguish study Bible content from the base translation text, a small set of additional USFM markers are used to indicate the beginning and ending point of the extended study content types.

.. toctree::
	:maxdepth: 1

	Extended Book Introductions <intros_book>
	Division and Section Introductions <intros_div>
	Extended Footnotes <efnotes>
	Extended Cross References <exrefs>
	Sidebars <sidebars>

A set of study Bible :doc:`content categories <categories>` can be defined and inserted into any study content type using the ``\cat ...\cat*`` markers.

.. toctree::
	:hidden:

	Content Categories <categories>

.. note::

	**Important Notes:** The use of USFM markup for study Bible authoring is supported by an editing environment which understands the structure of study additions to a standard USFM  scripture translation text. Paratext 7.3 and beyond provides support for study Bible content authoring through an enhanced multi-pane editing window. A project must be initiated in Paratext specifically as a Study Bible project in order to have these enhancements enabled.

	Study Bible projects initiated in earlier versions of Paratext will have used a multiple project arrangement in order to manage the various study content items. These projects will need to be merged into a single study Bible project in order to make use of the enhanced editor in Paratext 7.3. Paratext 7.3 provides a software tool to assist with merging multi-project study Bible contents.

	Please ask your Paratext supporter for additional help with initial study Bible setup and configuration. Paratext Helps on working with study Bibles, and a Study Bible Authoring guide are also available to registered users from the Paratext `website <http://paratext.org>`_.
