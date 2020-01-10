.. include:: /_static/inc_styles.txt

.. index:: study content; cross references, extended cross references, study cross reference

Extended Cross References
=========================

.. index:: extended cross reference; container, study cross reference; container

.. rubric:: Extended Cross Reference Container

The **extended (study) cross references** are inserted inline within the study project text using the following general syntax. The boundaries of the cross reference text are defined by an opening and closing marker. The remainder of the cross reference is written using standard USFM :ref:`cross reference content element <usfmn_x-content>` markers.

.. _usfmn_ex:
.. index:: marker; \ex ...\ex*, cross reference; study cross reference

\\ex ...\\ex\*
--------------

:Syntax: ``\ex_+_(\xo_REF_)cross reference content\ex*``
:Type: extended note
:Added: 2.3
:Use: Beginning and ending of the extended cross reference element.

:red:`+`

* The cross reference caller, which may be one of the following three types:

	    :red:`+` – indicates that the caller should be generated automatically by the translation editor, or publishing tools. |br|
	    :red:`-` – indicates that no caller should be generated, and is not used. |br|
	    :red:`?` – where ? represents the character to be used for the caller. The caller is defined for the specific cross reference by the author.

:red:`cross reference content` (see :ref:`below <usfmn_x-content>`)

	* All of the text elements which make up the extended cross reference. Refer to the documentation on using standard USFM :ref:`cross reference content element <usfmn_x-content>` markers.
