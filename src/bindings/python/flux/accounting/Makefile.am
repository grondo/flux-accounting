acctpy_PYTHON = \
	__init__.py \
	accounting_cli_functions.py \
	job_archive_interface.py \
	create_db.py \
	print_hierarchy.py

dist_fluxcmd_SCRIPTS = \
	flux-account.py

clean-local:
	-rm -f *.pyc *.pyo
	-rm -rf __pycache__

TESTSCRIPTS = \
	test/test_bank_subcommands.py \
	test/test_create_db.py \
	test/test_example.py \
	test/test_job_archive_interface.py \
	test/test_user_subcommands.py

dist_check_SCRIPTS = \
	$(TESTSCRIPTS)

TESTS = $(TESTSCRIPTS)

AM_TESTS_ENVIRONMENT = \
	export PYTHONPATH="$(abs_top_srcdir)/src/bindings/python/:$(abs_top_srcdir)/t/pycotap:$(PYTHON_SITE_PKG):$$PYTHONPATH";\
	export PYTHON="${PYTHON}";

TEST_EXTENSIONS = .py
PY_LOG_DRIVER = $(PYTHON) $(top_srcdir)/config/tap-driver.py
