^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package rostful
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.0.10 (2016-08-25)
-------------------
* Update tutorial.rst
* adding talker tutorial
* Merge pull request `#80 <https://github.com/asmodehn/rostful/issues/80>`_ from asmodehn/reverse_proxy
  allowing rostful to run behind a reverse proxy.
* removed test link from template.
* allowing rostful to run behind a reverse proxy.
* now changing NaN to null in every response.
  cosmetics.
* Merge pull request `#75 <https://github.com/asmodehn/rostful/issues/75>`_ from asmodehn/handle_nan
  using simplejson to be able to change nan from python to null in json…
* using simplejson to be able to change nan from python to null in json, since NaN is not valid json.
* quick fix service and topic type introspection.
* fixing GET request to backend ros services (disabling full and json arguments, parser seems somehow broken)
  fixing GET request with _rosdef suffix
* Merge pull request `#74 <https://github.com/asmodehn/rostful/issues/74>`_ from asmodehn/cleanup
  cleanup while unifying code design with task planner.
* cleanup while unifying code design with task planner.
* removed import of flask_security, which we don't use anymore.
* adding support for message type Header  in template.
* fixing install rules. cleanup migrations.
* Merge pull request `#73 <https://github.com/asmodehn/rostful/issues/73>`_ from asmodehn/removing_rocon_features
  Removing rocon features
* cleaning up obsolete arguments from ros launcher.
* removind security / login / db form here.
  probably the wrong place and time to try that.
* fix issue with leading "/" not being added to the rosname we get from url.
  fixing all tests to pass, een if they are still empty.
* fixed basic app tests with and without pyros connection.
* Merge branch 'first_unittests' into removing_rocon_features
  Conflicts:
  rostful/flask_views.py
  rostful/server.py
* improved design following flask documentation. but templates not found for tests.
* extracted wsgi app from server.
  started wsgi unittest with testapp working. much more work to be done.
  cleaning up and cosmetics.
* cleanup in progress, mostly working.
  wait for tests before merging into main branch.
* Merge branch 'indigo' into indigo-devel
  Conflicts:
  package.xml
* adding sqlalchemy as dependency
* Merge branch 'indigo' of https://github.com/asmodehn/rostful into indigo
  Conflicts:
  deps/testfixtures
* adding python-wtforms as ros dependency
  Conflicts:
  rostful/deps/testfixtures
* adding python-wtforms as ros dependency
* Merge pull request `#66 <https://github.com/asmodehn/rostful/issues/66>`_ from asmodehn/pyros_fixes
  now passing basepath to pyros context for ros dynamic setup if needed
* Merge branch 'indigo-devel' of https://github.com/asmodehn/rostful into pyros_fixes
  Conflicts:
  launch/rostful.launch
* adding doc for cache topics args.
* now passing basepath to pyros context for ros dynamic setup if needed
* new connection cache feature disabled by default
* adding option to enable cache or not from rosparams.
* adding remap arguments, useful if using connection_cache
* Contributors: AlexV, Marcus Liebhardt, alexv

0.0.9 (2016-01-28)
------------------
* Merge tag '0.0.9' into indigo
  Conflicts:
  deps/testfixtures
* Merge pull request `#65 <https://github.com/asmodehn/rostful/issues/65>`_ from asmodehn/tests_setup
  Tests setup
* fixing pyrosexception import.
* attempting travis fix.
* a beginning of documentation, and getting ready for 0.1 release...
* handling service timeout and not found as exception to return correct error status.
* fixing rester test for topics. now passing.
* fixed http response for mute publishers.
  added rester tests for topics.
  cosmetics.
* adding rester tests to be run with rostest to verify rostful behavior with pyros testnodes.
  fixing roster script to strip useless rosargs from rostest run.
* small refactoring to make testing rostful easier.
* Merge pull request `#61 <https://github.com/asmodehn/rostful/issues/61>`_ from asmodehn/pyros0.2_adapt
  Pyros 0.1 migration
* cosmetics.
* improving exception catching and fowarding to web client.
* removing check for allow_pub / allow_sub. authorization should not be done here.
* fixed for changes to pyros version 0.1
* Starting to get topics and services list with pyros 0.1
* fixing rosinstall files given new workspace structure for examples
* Merge pull request `#58 <https://github.com/asmodehn/rostful/issues/58>`_ from asmodehn/new_catkin
  New catkin
* Merge pull request `#57 <https://github.com/asmodehn/rostful/issues/57>`_ from asmodehn/indigo-devel
  updating indigo before dependency refactoring
* bumping reverted flask-restful
* bumping modified passlib and flask-restful
* adding all dependencies as submodules and getting rostful to work again without flask-ext-catkin
* removing examples, since they are now in a separate repository
* adding a lot of dependencies from flask-ext-catkin
* reorganizing documentation
* merging old markdown doc into RST doc
* removed useless mercurial file
* moving everything one folder down
* moved examples. removed src/. fixed setup.py
* commenting rester package and dependencies as they make problems on build at the moment.
* adding symlink in src to workaround catkin < 0.6.15 package_dir issue.
* Merge branch 'rester' into indigo-devel
* Merge pull request `#55 <https://github.com/asmodehn/rostful/issues/55>`_ from asmodehn/empty_request_improve
  handle empty request properly now
* handle empty request properly now
* Merge branch 'indigo-devel' of https://github.com/asmodehn/rostful into rester
  Conflicts:
  rostful/rostful/flask_views.py
* adding content_type if service returns None
* Merge branch 'indigo-devel' of https://github.com/asmodehn/rostful into rester
* Merge branch 'indigo' of https://github.com/asmodehn/rostful into rester
* fixing setup.py for install.
* Merge branch 'indigo-devel' of https://github.com/asmodehn/rostful into rester
* removed obsolete sample code
* bumping rester to be able to call apirunner form python
* fixing response to set content-type properly
* adding bool implementation for msg params in frontend
* Merge pull request `#53 <https://github.com/asmodehn/rostful/issues/53>`_ from asmodehn/travis
  Travis
* adding travis badge
* fixing travis build, only for rostful package
* starting travis integration
* adding Rester for tests. fixed content type on backend. first tests working
* Merge pull request `#51 <https://github.com/asmodehn/rostful/issues/51>`_ from asmodehn/params
  integrating params. backend has been tested. frontend not there yet.
* integrating params. backend has been tested. frontend not there yet.
* fixing roslaunch instructions.
* Contributors: AlexV, alexv

0.0.8
-----
* Extracted multiprocess mess from this package. Trying to keep this a neat python (flask) web REST backend.

0.0.2
-----
* Converted to Catkin
* Migrated from raw python to Flask
* Added Celery Support for async tasks
* Experimental Rocon support
