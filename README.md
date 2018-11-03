[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)

This repository is intended to be a prototype for *rule repositories*
used by [Interlibr](https://github.com/Xalgorithms/interlibr). It
follows a basic structure:

Every top-level directory is intended to be a *namespace* in
[Xalgo](https://github.com/Xalgorithms/general-documentation/blob/master/xalgo.md)
terms.
  
The namespace directory can contain .rule, .table or .json files. The
.rule files will be interpreted as Xalgo expressions. The .table files
contain meta-information about tables that are made available within
Interlibr. If there are *DATA* statements in the .table files
referencing *local* .json files, then the table will be populated with
data from those files.

If there are top-level directories that **are not namespaces** then
*namespaces.txt* can be used as a white-list to indicate which
directories should be considered namespaces.
&Omega;