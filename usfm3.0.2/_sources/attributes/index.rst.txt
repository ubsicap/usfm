.. include:: /_static/inc_styles.txt

.. index:: word level attributes, marker attributes, attributes

Word Level Attributes
=====================

|badge_3.0|

USFM 3.0 provides a general syntax for adding named attributes to character markers. Attributes define additional properties of the marked content. The addition of marker attributes is a means of extending the meta information contained within in a USFM text.

USFM will *formally* provide descriptive attributes for a :ref:`subset <attributes_markersProviding>` of character markers. Each marker in this set will have a defined list of attributes, which are relevant to the overall purpose of the marker.

.. _attributes_syntax:
.. index:: attributes; syntax

General Syntax
^^^^^^^^^^^^^^

Within a character marker span, an attributes list is separated from the text content by a vertical bar ``|``. Attributes are listed as pairs of **name** and corresponding **value** using the syntax: ``attribute="value"``. The attribute name is a single ASCII string. The value is wrapped in quotes.

**Example:**

.. code-block:: text

    \w gracious|lemma="grace"\w*

.. _attributes_default:
.. index:: attributes; default

Default Attribute
^^^^^^^^^^^^^^^^^

When content is supplied in the position of a marker attribute, but without an explicit attribute name, the USFM specification defines a single default. Defaults are only provided for :ref:`markers <attributes_markersProviding>` which formally provide attributes in the current version of USFM.

**Example:**

.. code-block:: text

    \w gracious|grace\w*

... where the default attribute for ``\w ...\w*`` is defined as being "lemma". This allows a commonly used attribute (the default) to be expressed with as little additional markup as possible within the text.

.. _attributes_multiValues:
.. index:: attributes; multiple values

Multiple Attribute Values
^^^^^^^^^^^^^^^^^^^^^^^^^

In cases where more than one value should be provided for an attribute key, the author should provide a comma separated list within the value string. Leading and trailing space characters adjacent to the comma separators are ignored.

**Example:**

.. code-block:: text

    \w gracious|strong="H1234,G5485"\w*

|ico_see| See the attributes for :ref:`\\w ...\\w\* <usfmc_w-attr>` for additional examples.

.. _attributes_multiParts:
.. index:: attributes; multiple parts

Multiple Attribute Parts
^^^^^^^^^^^^^^^^^^^^^^^^

In cases where an attribute value is composed of multiple parts (e.g. a compound word or phrase), the author can (optionally) separate the parts using a colon ``:`` within the value string.

|ico_see| See the ``gloss`` attribute for :ref:`\\rb ...\\rb\* <usfmc_rb-attr>` an example of the use of this syntax.

.. _attributes_backward:
.. index:: attributes; backward compatibility

Backward Compatibility
^^^^^^^^^^^^^^^^^^^^^^

Any pre-existing markers which formally provide attributes in USFM 3.0 (or newer) may always continue to be used “un-decorated” (without attributes). ``\w gracious\w*`` remains valid USFM content.

.. _attributes_userDefined:
.. index:: attributes; user-defined

User Defined Attributes
^^^^^^^^^^^^^^^^^^^^^^^

Using the general syntax, attributes may be added to any character markers beyond the formally provided set for the current version of USFM. These will not be considered strictly USFM compliant, and there is no assurance that they will be supported by compliant software tools or processes. Future versions of USFM may formally provide additional attributes.

Any user defined attributes must begin with the prefix ``x-``.

**Examples:**

.. code-block:: text

	\w gracious|x-myattr="metadata"\w*
	\w gracious|lemma="grace" x-myattr="metadata"\w*

.. _attributes_markersProviding:
.. index:: attributes; markers providing

Character Markers Providing Attributes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* :ref:`\\w ...\\w\* <usfmc_w-attr>` (``lemma``, ``strong``, ``srcloc``)
* :ref:`\\rb ...\\rb\* <usfmc_rb-attr>` (``gloss``)
* :ref:`\\xt ...\\xt\* <usfmc_xt-attr>` (``link-href`` - a :doc:`linking attribute </linking/index>`)
* :ref:`\\fig ...\\fig\* <usfmc_fig-attr>` (``alt``, ``src``, ``size``, ``loc``, ``copy``, ``ref``) - harmonizing the USFM 2.x syntax for this marker with this attribute specification
