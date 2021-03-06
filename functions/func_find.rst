.. MusicBrainz Picard Documentation Project

$find
=====

| Usage: **$find(haystack,needle)**
| Category: text
| Implemented: Picard 2.3

**Description:**

Returns the zero-based index of the first occurrence of ``needle`` in ``haystack``, or
an empty string if ``needle`` was not found.  The comparisons are case-sensitive. If ``needle`` is
blank, it will match the beginning of ``haystack`` and return "0". The function does not
support wildcards.

.. note::

    Prior to Picard 2.3.2 ``$find`` returned "-1" if ``needle`` was not found.


**Example:**

The following statements will return the values indicated::

    $find(abcdef,a)     ==>  "0"
    $find(abcdef,c)     ==>  "2"
    $find(abcdef,cd)    ==>  "2"
    $find(abcdef,g)     ==>  ""
    $find(abcdef,B)     ==>  ""
    $find(,a)           ==>  ""
    $find(abcdef,)      ==>  "1"
