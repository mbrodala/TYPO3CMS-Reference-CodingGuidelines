.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../../Includes.txt


Extension directory structure
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

An extension directory contains the following files and directories:


.. ### BEGIN~OF~TABLE ###

.. container:: table-row

   Name
         Name

   Description
         Description


.. container:: table-row

   Name
         ext\_emconf.php

   Description
         This is the only mandatory file in the extension. It describes
         extension to the rest of TYPO3.


.. container:: table-row

   Name
         ext\_icon.gif

   Description
         This is icon of the extension. The name may not be changed.


.. container:: table-row

   Name
         ext\_localconf.php

   Description
         This file contains hook definitions and plugin configuration. The name
         may not be changed.


.. container:: table-row

   Name
         ext\_tables.php

   Description
         This file contains table declarations. For more information about
         table declarations and definitions see the “TYPO3 Core API” document.
         The name may not be changed.


.. container:: table-row

   Name
         ext\_tables.sql

   Description
         This files contains definitions for extension tables. The name may not
         be changed.

         The file may contain either a full table definition or a partial
         table. The full table definition declares extension's tables. It looks
         like a normal SQL CREATE TABLEstatement.

         The partial table definition contains a list of the fields that will
         be added to the existing table. Here is an example::

            CREATE TABLE pages (
                   tx_myext_field int(11) DEFAULT '0' NOT NULL,
            );

         Notice the comma after the field. In the full table definition it will
         be a error but in the partial table definition it is required. TYPO3
         will merge this table definition to the existing table definition when
         comparing expected and actual table definitions. Partial definitions
         can also contain indexes and other directives. They can also change
         existing table fields though it is not recommended because it may
         create problems with the TYPO3 core and/or other extensions.

         TYPO3 parses ext\_tables.sqlfiles. TYPO3 expects that all table
         definitions in this file look like the ones produced by the
         mysqldumputility. Incorrect definitions may not be recognized by the
         TYPO3 SQL parser.


.. container:: table-row

   Name
         tca.php

   Description
         This file contains full table definitions for extension tables.


.. container:: table-row

   Name
         locallang\*.xml

   Description
         These files contains localizable labels. They can also appear in
         subdirectories.


.. container:: table-row

   Name
         doc/

   Description
         This directory contains the extension manual. The name may not be
         changed.


.. container:: table-row

   Name
         doc/manual.sxw

   Description
         This file contains extension manual in OpenOffice 1.0 format. The name
         or file format may not be changed. See the “Documentation template”
         document on typo3.orgfor more information about extension manuals.


.. container:: table-row

   Name
         piX/

   Description
         These directories contain Frontend plugins. If extension is generated
         by the Kickstarter, :code:`*X*` will be a number. It is recommended to
         give more meaningful names to Frontend plugin directories.


.. container:: table-row

   Name
         svX/

   Description
         These directories contain TYPO3 services. If extension is generated by
         the Kickstarter, :code:`*X*` will be a number. It is recommended to
         give more meaningful names to service directories.


.. container:: table-row

   Name
         modX/

   Description
         These directories commonly contain Backend modules. If extension is
         generated by the Kickstarter, :code:`*X*` will be substituted with a
         number. It is recommended to give more meaningful names to Backend
         module directories.


.. container:: table-row

   Name
         modfuncX/

   Description
         These directories commonly contain Backend submodules (embedded into
         other modules). If extension is generated by the Kickstarter,
         :code:`*X*` will be a number. It is recommended to give more
         meaningful names to these directories.


.. container:: table-row

   Name
         lib/

   Description
         Directory for non–TYPO3 files supplied with extension. TYPO3 is
         licensed under GPL version or 2 or any later version. Any non–TYPO3
         code must be compatible with GPL version 2 or any later version. Note:
         this name is not mandatory but recommended.


.. ###### END~OF~TABLE ######


This directory structure is  **strongly**  **recommended** .
Extensions may create their own directories (for example, move all
language files into other directories).
