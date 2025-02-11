==================================
Sale Order Invoicing Finished Task
==================================

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:502e4a51404a43bacacc17832b0b37a42f1efbeab431c13e7eb8e4708fbfc5f2
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fsale--workflow-lightgray.png?logo=github
    :target: https://github.com/OCA/sale-workflow/tree/12.0/sale_order_invoicing_finished_task
    :alt: OCA/sale-workflow
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/sale-workflow-12-0/sale-workflow-12-0-sale_order_invoicing_finished_task
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/sale-workflow&target_branch=12.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

The requirement of this module is to give the possibility in the task to
indicate if a task is available to invoice or not. This means by default even
the task is not finished you could set it as invoiceable.

As an option you can relate to a Project Stage ( ``project.task.type`` ) this
control. For example if you want to assign Invoiceable to stage ``Done`` always.

**Table of contents**

.. contents::
   :local:

Usage
=====

To use this module, you need to:

1. Go to Sales -> Product and create a service product

2. In the product go to Sales tab > Invoicing section and select
   (1) An invocing policy (2) Track service must be create a task and
   tack hours (3) Set 'Invoicing control by task' checkbox and save


   .. image:: https://raw.githubusercontent.com/OCA/sale-workflow/12.0/sale_order_invoicing_finished_task/static/description/product_view_invoicefinishedtask.png


3. Go to Sales -> Sale orders -> Create a new one. Add a customer and the
   product you have created
4. Confirm the sales order, it will create you a project and a task
5. Go to the task and you will find a smartbutton called Not invoiceable, when
   you press the button you will indicate that the task can be invoiced

   .. image:: https://raw.githubusercontent.com/OCA/sale-workflow/12.0/sale_order_invoicing_finished_task/static/description/task_view_invoicefinishedtask.png

   If the product is configured with an invoicing policy = Order, then the
   delivered quantity is set to the ordered quantity. Otherwise, the time spent
   on the task is used.

6. Optional: if you want to use project stages to control this Go To
   Project -> Configuration -> Stages -> You have to set true the field
   Invoiceable in the stages that you consider are invoiceable. Event to use
   stages for this functionality you can also set it manually in the task
   whenever you want.

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/sale-workflow/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/sale-workflow/issues/new?body=module:%20sale_order_invoicing_finished_task%0Aversion:%2012.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Tecnativa
* Camptocamp

Contributors
~~~~~~~~~~~~

* Denis Leemann <denis.leemann@camptocamp.com>
* `Tecnativa <https://www.tecnativa.com>`_:

  * Sergio Teruel
  * Carlos Dauden
  * Alexandre Díaz

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

This module is part of the `OCA/sale-workflow <https://github.com/OCA/sale-workflow/tree/12.0/sale_order_invoicing_finished_task>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
