Compute API
+++++++++++

This repository is now frozen-in-time and will not accept new patches.

It was the original API information holder for the OpenStack Compute project,
also known as Nova. The Nova project provides open source cloud management and
orchestration services.

Prerequisites
=============
`Apache Maven <http://maven.apache.org/>`_ must be installed to build the
documentation.

To install Maven 3 for Ubuntu 12.04 and later,and Debian wheezy and later::

    apt-get install maven

On Fedora 15 and later::

    yum install maven3

Building
========

The manuals are in the ``incubation``, ``openstack-compute-api-1.0``
and ``openstack-compute-api-2`` directories.

To build a specific guide, look for a ``pom.xml`` file within a subdirectory,
then run the ``mvn`` command in that directory. For example::

    cd openstack-compute-api-2
    mvn clean generate-sources


Testing of changes and building of the manual
=============================================

Install the python tox package and run ``tox`` from the top-level
directory to use the same tests that are done as part of our Jenkins
gating jobs.

If you like to run individual tests, run:

 * ``tox -e checkniceness`` - to run the niceness tests
 * ``tox -e checksyntax`` - to run syntax checks
 * ``tox -e checkdeletions`` - to check that no deleted files are referenced
 * ``tox -e checkbuild`` - to actually build the manual

tox will use the `openstack-doc-tools package
<https://github.com/openstack/openstack-doc-tools>`_ for execution of
these tests. openstack-doc-tools has a requirement on maven for the
build check.

Contributing
============

Our community welcomes all people interested in open source cloud
computing, and there are no formal membership requirements. The best
way to join the community is to talk with others online or at a meetup
and offer contributions through Launchpad, the OpenStack wiki, or
blogs. We welcome all types of contributions, from blueprint designs
to documentation to testing to deployment scripts.

Installing
==========

Refer to http://docs.openstack.org to learn more about installing an
OpenStack Compute server that can respond to these API commands.
