.. include:: /_static/inc_styles.txt

.. index:: tables

Tables
======

.. _usfmp_tr:
.. index:: marker; \tr, tables; table row start

\\tr
^^^^

:Syntax: ``\tr_``
:Type: paragraph
:Added: 1.0
:Use: Table row start. |br|
	The first ``\tr`` initiates a new table. |br|
	Rows contain column :ref:`headings <usfmc_th#>` or :ref:`cells <usfmc_tc#>`.

-----

.. _usfmc_th#:
.. index:: marker; \th#, tables; table column heading

\\th#
^^^^^

:Syntax: ``\th#_text...``
:Type: character
:Added: 1.0 (updated 3.0 - column spanning)
:Use: Table column heading. |br|
	The variable # represents the table column number. |br| |br|
	|badge_3.0| Use a dash ``-`` between a range of column numbers to indicate that the columns should be spanned.

.. _usfmc_thr#:
.. index:: marker; \thr#, tables; right aligned table column heading

\\thr#
^^^^^^

:Syntax: ``\thr#_text...``
:Type: character
:Added: 1.0 (updated 3.0 - column spanning)
:Use: Right aligned table column heading. |br|
	The variable # represents the table column number. |br| |br|
	|badge_3.0| Use a dash ``-`` between a range of column numbers to indicate that the columns should be spanned.

**Text and Formatting Samples** - Numbers 7.12-83 (GNT)

.. code-block:: text
	:name: usfm-character_th#_example
	:emphasize-lines: 3

	\p
	\v 12-83 They presented their offerings in the following order:
	\tr \th1 Day \th2 Tribe \th3 Leader
	\tr \tcr1 1st \tc2 Judah \tc3 Nahshon son of Amminadab
	\tr \tcr1 2nd \tc2 Issachar \tc3 Nethanel son of Zuar
	\tr \tcr1 3rd \tc2 Zebulun \tc3 Eliab son of Helon
	\tr \tcr1 4th \tc2 Reuben \tc3 Elizur son of Shedeur
	\tr \tcr1 5th \tc2 Simeon \tc3 Shelumiel son of Zurishaddai
	...

.. image:: images/usfm-character_th.jpg
	:width: 250px

Numbers 2.10-16 (GNT)

.. code-block:: text
	:name: usfm-character_thr#_example
	:emphasize-lines: 4

	\p
	\v 10-16 On the south, those under the banner of the division of Reuben shall camp in 
	their groups, under their leaders, as follows:
	\tr \th1 Tribe \th2 Leader \thr3 Number
	\tr \tc1 Reuben \tc2 Elizur son of Shedeur \tcr3 46,500
	\tr \tc1 Simeon \tc2 Shelumiel son of Zurishaddai \tcr3 59,300
	\tr \tc1 Gad \tc2 Eliasaph son of Deuel \tcr3 45,650
	\tr \tcr1-2 Total: \tcr3 151,450

.. image:: images/usfm-character_thr.jpg
	:width: 250px

-----

.. _usfmc_tc#:
.. index:: marker; \tc#, tables; table cell

\\tc#
^^^^^

:Syntax: ``\tc#_text...``
:Type: character
:Added: 1.0 (updated 3.0 - column spanning)
:Use: Table cell. |br|
	The variable # represents the table column number. |br| |br|
	|badge_3.0| Use a dash ``-`` between a range of column numbers to indicate that the columns should be spanned.

.. _usfmc_tcr#:
.. index:: marker; \tcr#, tables; right aligned table cell

\\tcr#
^^^^^^

:Syntax: ``\tcr#_text...``
:Type: character
:Added: 1.0 (updated 3.0 - column spanning)
:Use: Right aligned table cell. |br|
	The variable # represents the table column number. |br| |br|
	|badge_3.0| Use a dash ``-`` between a range of column numbers to indicate that the columns should be spanned.

**Text and Formatting Sample** - Numbers 2.10-16 (GNT)

.. code-block:: text
	:name: usfm-character_tc#_example
	:emphasize-lines: 5-8

	\p
	\v 10-16 On the east side, those under the banner of the division of Judah shall camp in 
	their groups, under their leaders, as follows:
	\tr \th1 Tribe \th2 Leader \thr3 Number
	\tr \tc1 Judah \tc2 Nahshon son of Amminadab \tcr3 74,600
	\tr \tc1 Issachar \tc2 Nethanel son of Zuar \tcr3 54,400
	\tr \tc1 Zebulun \tc2 Eliab son of Helon \tcr3 57,400
	\tr \tcr1-2 Total: \tcr3 186,400

.. image:: images/usfm-character_tc.jpg
	:width: 250px

.. _usfmc_table_colspan:
.. index:: tables; column span

.. warning:: 

	**Empty table cells:**
	An empty table cell still requires a corresponding marker in the table text. Alternatively, indicate that a cell spans multiple columns by indicating a column range ``\tr \tcr1-2 Total: \tcr3 151,450``.