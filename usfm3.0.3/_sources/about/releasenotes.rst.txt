.. include:: /_static/inc_styles.txt

.. index:: release notes

Release Notes
=============

.. contents::
    :local:
    :depth: 2

-----

.. _about_release_3.0.1:

3.0.1
^^^^^

*January 2020*

This update is primarily for providing documentation fixes, as well as minor updates to Paratext stylesheets (enable PT9 ColorNames feature; allow ``\xt`` in more contexts)

.. _about_release_3.0:

3.0
^^^

USFM 3.0 additions or revisions are highlighted throughout this documentation using the badge |badge_3.0|

*April 2018*

**Marker Additions**

* USFM version identifier: :ref:`\\usfm <usfmp_usfm>`
* Alternate language table of contents texts: :ref:`\\toca# <usfmp_toc#>`
* List of witnesses in footnotes (for critical editions): :ref:`\\fw ...\\fw* <usfmc_fw>`
* Target references "added" text: :ref:`\\xta ...\\xta* <usfmc_xta>`
* Superscript: :ref:`\\sup ...\\sup* <usfmc_sup>`
* Translator's section (chunk) milestones: :ref:`\\ts-s\\* and \\ts-e\\* <usfmm_ts-s>`

**Marker Revisions**

* Revised syntax for ruby glosses (CJK texts): :ref:`\\rb ...\\rb\* <usfmc_rb>`

    * Add :doc:`descriptive attribute </attributes/index>` ``gloss`` for :ref:`\\rb ...\\rb\* <usfmc_rb-attr>`

* Added default ``link-href`` :doc:`linking attribute </linking/index>` for :ref:`\\xt ...\\xt\* <usfmc_xt-attr>`
* Changed common :ref:`attributes for milestones <milestones_attributes>`:

    * Replace single ``id`` with separate start ``sid`` and end ``eid`` milestone attributes. |br| This update aligns USFM with the corresponding single `<ms> <https://ubsicap.github.io/usx/elements.html#ms>`_ milestone element in USX, where the ``id`` attribute content would not be unique for `<ms> <https://ubsicap.github.io/usx/elements.html#ms>`_.

* Changed name of :doc:`linking attribute </linking/index>` ``link-name`` to ``link-id``.
* *Restored* :ref:`\\pr <usfmp_pr>` for use as "text refrain".

**Syntax and Features**

* Clarify and support syntax for :ref:`standalone milestones <milestones_standalone>`.
* Document best practice for attributes containing :ref:`multiple values <attributes_multiValues>`, or :ref:`multiple parts <attributes_multiParts>` (see the ``gloss`` attribute for :ref:`\\rb ...\\rb\* <usfmc_rb-attr>`)

.. _about_release_3.0rc1:

3.0rc1
^^^^^^

*October 2016*

**Marker Additions**

* Letter opening: :ref:`\\po <usfmp_po>`
* List header and footer elements: :ref:`\\lh <usfmp_lh>` and :ref:`\\lf <usfmp_lf>`
* Embedded list: :ref:`\\lim# <usfmp_lim#>`
* Hebrew note: :ref:`\\qd <usfmp_qd>`
* Semantic division: :ref:`\\sd# <usfmp_sd#>`
* Aramaic wordlist entry: :ref:`\\wa ...\\wa\* <usfmc_wa>`
* Geographic proper name (Chinese texts): :ref:`\\png ...\\png\* <usfmc_png>`
* Target references "added" text: :ref:`\\xta ...\\xta\* <usfmc_xta>`
* Published cross reference origin text: :ref:`\\xop ...\\xop\* <usfmc_xop>`
* Structured list items: :ref:`\\lik ...\\lik\* <usfmc_lik>` and :ref:`\\liv# ...\\liv#\* <usfmc_liv#>`
* List item total: :ref:`\\litl ...\\litl\* <usfmc_litl>`
* Link text: :ref:`\\jmp ...\\jmp\* <usfmc_jmp>`
* Common peripheral :ref:`identifiers <periph_div>`
* Ruby glosses (CJK texts): :ref:`\\rb ...\\rb\* <usfmc_rb>`
* Quotation start / end milestones: :ref:`\\qt#-s\\* and \\qt#-e\\* <usfmm_qt#-s>`

**Marker Revisions**

* Support citation form for wordlist / glossary text (update :ref:`\\w ...\\w\* <usfmc_w>`).
* Support for explicit :ref:`table cell <usfmc_tc#>` column :ref:`spanning <usfmc_table_colspan>`.
* Revised syntax for figures / illustrations applying descriptive :doc:`attributes </attributes/index>`: :ref:`\\fig ...\\fig\* <usfmc_fig-attr>`
* *Deprecated* cross reference and footnote DC content markers: :ref:`\\xdc ...\\xdc\* <usfmc_xdc>` and :ref:`\\fdc ...\\fdc\* <usfmc_fdc>`
* *Deprecated* combined marker for proper name within translator's addition: :ref:`\\addpn ...\\addpn\* <usfmc_addpn>`
* *Deprecated* numbered running header: :ref:`\\h# <usfmp_h>`
* *Deprecated* pronunciation info marker: :ref:`\\pro ...\\pro\* <usfmc_pro>` in favour of :ref:`ruby annotations <usfmc_rb>` proposal.

**Syntax and Features**

* Syntax for assigning word-level :doc:`descriptive attributes </attributes/index>`.

    - Descriptive attributes for :ref:`\\w ...\\w\* <usfmc_w-attr>`
    - Descriptive attributes for :ref:`\\fig ...\\fig\* <usfmc_fig-attr>`

* Syntax for assigning word-level :doc:`linking attributes </linking/index>`.
* Syntax for :doc:`milestones </milestones/index>`.

    - Quotation start / end milestones: :ref:`\\qt#-s\\* and \\qt#-e\\* <usfmm_qt#-s>`.

* Syntax for peripheral (:doc:`\\periph </peripherals/index>`) :ref:`identifiers <periph_id>`.

**Standard Reference**

* Clarify and document specification regarding :ref:`whitespace <syntax_whitespace>` and :ref:`new lines <syntax_newline>`.

.. _about_release_2.5:

2.5
^^^

*October 2013*

Validation (stylesheet) configuration update for Paratext 7.5 release.

.. _about_release_2.4:

2.4
^^^

*June 2013*

**Marker Additions**

* Support for :doc:`nesting character markup </characters/nesting>`.
 
Full support for the nested character markup syntax has been included in Paratext >=7.4, Publishing Assistant >=4.1, and the XML export format from Paratext known as "USX".

.. _about_release_2.35:

2.35
^^^^
*February 2012*

Primarily a documentation update.
 
Paratext 7.3 and beyond provides support for study Bible content authoring, within a single project text, through an enhanced multi-pane editing window. Earlier USFM documentation releases discussed study Bible content markup using one or two additional related project texts. This multi-project authoring configuration is no longer recommended now that there is workable authoring environment supporting a single-project study Bible text. Information relating to study Bible content markup and authoring practice in this documentation supersedes any reference to separate notes or sidebar projects in the earlier release notes (below).
 
* Deprecated ``\fs`` (footnote summary text) - not required when working within a single project study Bible text.

.. _about_release_2.3:

2.3
^^^
*July 2010*

Version numbers for the base USFM stylesheet and the study Bible notes and sidebars stylesheets have been synchronized to 2.3. This reflects the readiness of the Paratext 7.1 editor to support study Bible authoring.

**Marker Additions**

* Added study Bible cross reference marker :ref:`\\ex <usfmn_ex>` for adding additional cross-references to the notes project.

**Marker Revisions**

* *DEPRECATED* - Study Bible footnote marker ``\fs`` for marking a footnote summary text.
* Permit cross references to be added to the study Bible notes project.
* Revised markup specification for study Bible sidebars (now use any title, paragraph, poetry, table, or special text marker elements).

.. _about_release_2.2:

2.2
^^^
*October 2008*

**Marker Additions**

* Added character markers :ref:`\\xot ...\\xot\* <usfmc_xot>` and :ref:`\\xnt ...\\xnt\* <usfmc_xnt>` for uniquely marking target references to OT and NT passages (use of these markers is optional)
* Added :ref:`\\iqt ...\\iqt\* <usfmc_iqt>` to mark (scripture) quotations appearing in the introduction.

**Marker Revisions**

* :ref:`\\imte# <usfmp_imte#>` now includes an optional numeric variable (multiple levels).
* No-break space should now be marked using ~ (tilde), not !$

.. _about_release_2.1:

2.1
^^^
*April 2007*

**Marker Additions**

* Added :ref:`\\ili <usfmp_ili#>` for marking introduction list items.
* Reviewed and finalized Peripheral content markup:

    - Added new :doc:`back matter </peripherals/back>` books CNC, GLO, TDX, NDX.
    - Added INT book for scripture division :doc:`Introductions </peripherals/intros>`.
    - Updated scheme for marking content divisions in FRT, INT, BAK, OTH
    - Added various new content division markers.

**Marker Revisions**

* Finalized :doc:`Study Bible Content </notes_study/index>` markup.
* Reviewed and finalized Peripheral content markup (see "Marker Additions" above).
* Changed :ref:`\\rq ...\\rq\* <usfmc_rq>` from paragraph to character level markup.
* Changed :ref:`\\ca ...\\ca\* <usfmc_ca>` from paragraph to character level markup.

.. _about_release_2.05:

2.05
^^^^
*June 2006*

**Marker Additions**

* Added :ref:`\\rq <usfmc_rq>` for marking inline quotation references.

.. _about_release_2.04:

2.04
^^^^
*October 2005*

**Marker Additions**

* Added :ref:`\\toc3 <usfmp_toc#>` for providing the standard abbreviation for a book.

.. _about_release_2.03:

2.03
^^^^
*August 2005*

**Marker Additions**

* Added :ref:`\\toc1 <usfmp_toc#>` and :ref:`\\toc2 <usfmp_toc#>` for providing and marking long and short table of contents texts.
* Added :ref:`\\fl <usfmc_fl>` for marking footnote "label" text items.
* Added :ref:`\\fp <usfmc_fp>` for marking footnote additional paragraphs.

.. _about_release_2.0:

2.0
^^^
*October 2004*

The following sections outline changes in USFM from 1.53 to 2.0.

**Marker Revisions**

* Removed ``\pdi`` and ``\pde``, and substitute with embedded text markup (under additions, below)
* Removed ``\wr ...\wr*``. This was really a duplicate of :ref:`\\w ...\w\* <usfmc_w>` used for marking words in the scripture text which are included in the wordlist.
* Removed ``\ps``. This is used in conjunction with :ref:`\\nb <usfmp_nb>` to indicate that the paragraph spans the chapter boundary. It should be sufficient to just start the new chapter with :ref:`\\nb <usfmp_nb>` and use the appropriate paragraph marker for the previous chapter (:ref:`\\p <usfmp_p>`, :ref:`\\m <usfmp_m>` etc.)

**Marker Additions**

* Add character style :ref:`\\em ...\\em\* <usfmc_em>` for "emphasis".
* In Peripherals:

    - Add \\intro section to Front Matter (in addition to Preface).
    - Add \\maps (Maps Index) section to Back Matter.
    - Paratext will be adjusted to include predefined "standard" books for FRT, BAK, and OTH rather than using the book names XXA, XXB, and XXC for these materials.

* Add :ref:`\\sr <usfmp_sr>` for marking the text references range listed under a section heading :ref:`\\s <usfmp_s#>`.
* Add the following markers for "embedded text" (see example references – not all versions mark these items the same).

    - :ref:`\\pm <usfmp_pm>` - Embedded text paragraph
    - :ref:`\\pmo <usfmp_pmo>` - Embedded text opening
    - :ref:`\\pmc <usfmp_pmc>` - Embedded text closing
    - :ref:`\\pmr <usfmp_pmr>` - Embedded text refrain
    - :ref:`\\qm# <usfmp_qm#>` - Embedded text poetic line

* Add character style :ref:`\\pro ...\\pro\* <usfmc_pro>` for indicating pronunciation (in CJK texts).
* Add character style :ref:`\\wj ...\\wj\* <usfmc_wj>` for marking words of Jesus.
