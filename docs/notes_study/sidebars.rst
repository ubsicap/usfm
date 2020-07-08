.. include:: /_static/inc_styles.txt

.. index:: study content; sidebars, study content; articles, sidebars, articles

Sidebars
========

Sidebars may contain larger sections of topical content, or information for more in-depth study. This content is associated with a general area in the scripture reference text, but not necessarily a specific verse or word. Sidebars are inserted within the study project text using the following general syntax. The boundaries of the sidebar content are defined by an opening and closing marker. The remainder of the sidebar content is written using any USFM :doc:`title </titles_headings/index>`, :doc:`paragraph </paragraphs/index>`, :doc:`poetry </poetry/index>`, :doc:`table </tables/index>`, or :doc:`character </characters/index>` marker elements.

.. code-block:: text
	:name: usfm-study_sidebar_example
	:emphasize-lines: 1,4 

	\esb
	\ms Sidebar Title
	<sidebar content>
	\esbe

.. _usfmn_esb:
.. index:: marker; \esb

\\esb
^^^^^

:Syntax: ``\esb``
:Type: paragraph (extended note)
:Added: 2.1
:Use: Beginning (opening) of the sidebar content section.

.. rubric:: sidebar content

* All of the text elements which make up the sidebar content. Refer to the documentation on using standard USFM title, paragraph, poetry, table, or special text marker elements.
* Sidebars normally begin with an \\ms marker, used for providing a title to the sidebar content. 
* Illustrations can be added to sidebar content sections using the USFM \\fig ...\\fig\* marker.

.. _usfmn_esbe:
.. index:: marker; \esbe

\\esbe
^^^^^^

:Syntax: ``\esbe``
:Type: paragraph (extended note)
:Added: 2.1
:Use: End (closing) of the sidebar content.

.. note::

	**Important:** The normal USFM syntax for other note or character type markers which define content boundaries is to close the content section using a marker which is identical to the opening marker plus an added asterisk (e.g. :ref:`\\f ...\\f\* <usfmn_f>` or :ref:`\\ef ...\\ef\* <usfmn_f>`). The syntax for sidebar content does not follow this pattern. The closing marker is unique (\\esbe). This is necessary because the content of a sidebar contains many additional paragraph style types (and all other note types with content boundaries only contain character styles).

-----

.. rubric:: Text and Formatting Samples

Mark 1 (CEV Learning Bible)

.. code-block:: text
	:name: usfm-study_sidebars_example
	:emphasize-lines: 2,16

	\v 18 At once they left their nets and went with him.
	\esb \cat History\cat*
	\ms Fish and Fishing
	\p In Jesus' time, fishing took place mostly on lake Galilee, because Jewish people 
	could not use many of the harbors along the coast of the Mediterranean Sea, since these 
	harbors were often controlled by unfriendly neighbors. The most common fish in the Lake 
	of Galilee were carp and catfish. The Law of Moses allowed people to eat any fish with 
	fins and scales, but since catfish lack scales (as do eels and sharks) they were not to 
	be eaten (\xt Lev 11.9-12\xt*). Fish were also probably brought from Tyre and Sidon, 
	where they were dried and salted.
	...
	\p Among early Christians, the fish was a favorite image for Jesus, because the Greek 
	word for fish (\tl ichthus\tl*) consists of the first letters of the Greek words that 
	tell who Jesus is: \fig Ihsous Christos Theou Uios Swthr|alt="Christian Fish Image" 
	src="christfish.jpg" size="col" ref="1.18"\fig*
	\esbe
	\p\v 19 He went a little farther on and saw two other brothers, James and John, 
	the sons of Zebedee.

.. image:: images/usfm-study_sidebars.jpg
	:width: 350px