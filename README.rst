일단 제가 작업하면서 주로 참고했던 내용은 이 thread에 대부분 포함되어 있습니다.
https://github.com/pennersr/django-allauth/pull/2424
제가 알기로는 애플에서 client id는 bundle id와 service id 두 종류가 있는데, 앱을 통해 발급받은 token은 service id로만 인증이 가능해서 현재 이 값을 사용하도록 settings에 정의되어 있습니다.
웹을 통해 발급받은 token은 bundle id를 통해 인증해야 하는데, 현재 django-allauth 에서는 이 두개의 client id를 동시에 사용할 수 있도록 되어 있지 않은 상태인걸로 보입니다.. https://github.com/pennersr/django-allauth/issues/2718 여기에 비슷한 문제를 겪고 있는 issue가 있습니다.



==========================
Welcome to django-allauth!
==========================

.. image:: https://travis-ci.org/pennersr/django-allauth.svg
   :target: http://travis-ci.org/pennersr/django-allauth

.. image:: https://img.shields.io/pypi/v/django-allauth.svg
   :target: https://pypi.python.org/pypi/django-allauth

.. image:: https://coveralls.io/repos/pennersr/django-allauth/badge.svg?branch=master
   :alt: Coverage Status
   :target: https://coveralls.io/r/pennersr/django-allauth

.. image:: https://pennersr.github.io/img/bitcoin-badge.svg
   :target: https://blockchain.info/address/1AJXuBMPHkaDCNX2rwAy34bGgs7hmrePEr

.. image:: https://img.shields.io/badge/code%20style-pep8-green.svg
   :target: https://www.python.org/dev/peps/pep-0008/

.. image:: https://img.shields.io/badge/code_style-standard-brightgreen.svg
   :target: http://standardjs.com

.. image:: https://pennersr.github.io/img/emacs-badge.svg
   :target: https://www.gnu.org/software/emacs/

Integrated set of Django applications addressing authentication,
registration, account management as well as 3rd party (social) account
authentication.

Home page
  http://www.intenct.nl/projects/django-allauth/

Source code
  http://github.com/pennersr/django-allauth

Mailing list
  http://groups.google.com/group/django-allauth

Documentation
  https://django-allauth.readthedocs.io/en/latest/

Stack Overflow
  http://stackoverflow.com/questions/tagged/django-allauth

Rationale
=========

Most existing Django apps that address the problem of social
authentication focus on just that. You typically need to integrate
another app in order to support authentication via a local
account.

This approach separates the worlds of local and social
authentication. However, there are common scenarios to be dealt with
in both worlds. For example, an e-mail address passed along by an
OpenID provider is not guaranteed to be verified. So, before hooking
an OpenID account up to a local account the e-mail address must be
verified. So, e-mail verification needs to be present in both worlds.

Integrating both worlds is quite a tedious process. It is definitely
not a matter of simply adding one social authentication app, and one
local account registration app to your ``INSTALLED_APPS`` list.

This is the reason this project got started -- to offer a fully
integrated authentication app that allows for both local and social
authentication, with flows that just work.


Commercial Support
==================

This project is sponsored by IntenCT_. If you require assistance on
your project(s), please contact us: info@intenct.nl.

.. _IntenCT: http://www.intenct.info


Cross-Selling
=============

If you like this, you may also like:

- django-trackstats: https://github.com/pennersr/django-trackstats
- netwell: https://github.com/pennersr/netwell
