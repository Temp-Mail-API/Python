temp-mail
=========

Python API Wrapper for `temp-mail.org <https://temp-mail.org/>`_ service. Temp-mail is a service which lets you use anonymous emails for free. You can view full API specification in `api2.temp-mail.org <http://api2.temp-mail.org/>`_.

Requirements
------------

`requests <https://crate.io/packages/requests/>`_ - required.

`simplejson <https://crate.io/packages/simplejson/>`_ - optional, for a serious speed boost in JSON decode.

Installation
------------

Installing with pip::

    $ pip install temp-mail

Usage
-----

Get all emails from given email login and domain::

    from tempmail import TempMail

    tm = TempMail(login='denis', domain='@gnail.pw')
    api_host = 'privatix-temp-mail-v1.p.rapidapi.com'
    api_key='place_your_key_here'
    tm.set_header(api_host,api_key)
    print tm.get_mailbox()  # list of emails in denis@gnail.pw

Generate email address and get emails from it::

    from tempmail import TempMail

    tm = TempMail()
    api_host = 'privatix-temp-mail-v1.p.rapidapi.com'
    api_key='place_your_key_here'
    tm.set_header(api_host,api_key)
    email = tm.get_email_address()  # v5gwnrnk7f@gnail.pw
    print tm.get_mailbox(email)  # list of emails


.. image:: https://d2weczhvl823v0.cloudfront.net/saippuakauppias/temp-mail/trend.png
   :alt: Bitdeli badge
   :target: https://bitdeli.com/free

