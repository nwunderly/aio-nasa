.. currentmodule:: aionasa.apod

APOD API Reference
==================

This page provides a breakdown of the aionasa APOD module.

Parameters for APOD API:

- date: The date of the APOD image to retrieve. Defaults to 'today'.
- start_date: The first date to return when requesting a list of dates.
- end_date: The last date to return when requesting a list of dates. Range is inclusive.
- hd: Bool indicating whether to retrieve the URL for the high resolution image. Defaults to 'False'.
- concept_tags: DISABLED FOR THIS ENDPOINT.

.. note::
    If 'today' is used as the requested date (this is the default value) and the
    current date (according to UTC) does not have an APOD entry yet, the API will
    return a 404 and this library will raise a NotFound exception.
    If you would like to avoid this, you will need to catch the NotFound exception,
    and instead make a request for the previous day's APOD data.

Client
------

.. autoclass:: APOD
    :members:

Data Class
----------

.. autoclass:: AstronomyPicture
    :members: