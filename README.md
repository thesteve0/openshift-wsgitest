Wordpress on OpenShift
======================

This git repository is a Quickstart for a simple Python WSGI on OpenShift.

Running on OpenShift
----------------------------

Create an OpenShift account at http://openshift.redhat.com/

Create a Python application (you can call your application whatever you want)

    rhc app create -a wsgitest -t python-2.6

Add this repo

    cd wsgitest
    git remote add upstream -m master git://github.com/fallenpegasus/openshift-wsgitest.git
    git pull -s recursive -X theirs upstream master
    
Then push the repo upstream

    git push

That's it, you can now browse your application at:

    http://wsgi-$yournamespace.rhcloud.com

Notes
=====

This is grabbed from the MoinMoin project wiki/server/test.wsgi
written by Thomas Waldmann <tw@waldmann-edv.de>

Repackaged into OpenShift QuickStart form by Mark Atwood <matwood@redhat.com>

