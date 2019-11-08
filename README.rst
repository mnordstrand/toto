Data analysis
==============
- Document here the project: test
- Description: Project Description
- Data Source:
- Type of analysis:

Please document the project the better you can.

Stratup the project
=====================
The initial setup.

Create virtualenv and install the project::

  $ sudo apt-get install virtualenv python-pip python-dev
  $ deactivate; virtualenv ~/venv ; source ~/venv/bin/activate ;\
    pip install pip -U; pip install -r requirements.txt

Unittest test::

  $ make clean install test


Check for test in gitlab.com/{group}.
If your project is not set please add it:

- Create a new project on `gitlab.com/{group}/test`
- Then populate it:

  $ ##   e.g. if group is "{group}" and project_name is "test"
  $ git remote add origin git@gitlab.com:{group}/test.git
  $ git push -u origin master
  $ git push -u origin --tags

Functionnal test with a script::

  $ cd /tmp
  $ test-run

Install
==========
Go to `gitlab.com/{group}/test` to see the project, manage issues,
setup you ssh public key, ...

Create a python3 virtualenv and activate it::

  $ sudo apt-get install virtualenv python-pip python-dev
  $ deactivate; virtualenv -ppython3 ~/venv ; source ~/venv/bin/activate

Clone the project and install it::

  $ git clone gitlab.com/{group}/test
  $ cd test
  $ pip install -r requirements.txt
  $ make clean install test                # install and test

Functionnal test with a script::

  $ cd /tmp
  $ test-run

Continus integration
=====================
Every push of `master` branch will execute `.gitlab-ci.yml` docker jobs.

