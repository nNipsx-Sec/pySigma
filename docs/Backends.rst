Backends
########

Backends are responsible for conversion of Sigma rules into a target query languages. Mainly, they
have to convert the conditions of the Sigma rules with their reference to detection items into
equivalent query. Backends should not be used to handle log source types or data models, e.g. field
naming or differences in value representation. Use ::doc:`Processing_Pipelines` instead.

To implement a conversion for a new query language derive an appropriate backend base class from
below and override properties or methods as required.

Concepts
********

Conversion Methods
==================

Builtin Processing Pipeline
===========================

Output Formats
==============

Rule Finalization
-----------------

Output Finalization
-------------------

Classes
*******

Backend
=======

The backend base class is generic and can generate arbitrary output, e.g. Python data structures.

.. autoclass:: sigma.conversion.base.Backend
   :members:

TextQueryBackend
================

Backend base class for conversion to text based query languages. In many cases the methods doesn't
have to be overridden but string tokens have to be defined as class variable members (tbd).

.. autoclass:: sigma.conversion.base.TextQueryBackend
   :members: