# Package configuration
PROJECT = ci
COMMANDS = cmd/test
#CODECOV_TOKEN = your codecov token

# If you need to build more than one dockerfile, you can do so like this:
# DOCKERFILES = Dockerfile_filename1:repositoryname1 Dockerfile_filename2:repositoryname2 ...

# Including ci Makefile
CI_REPOSITORY ?= https://github.com/src-d/ci.git
CI_PATH ?= $(shell pwd)/.ci
MAKEFILE := $(CI_PATH)/Makefile.main
$(MAKEFILE):
	git clone --quiet --depth 1 $(CI_REPOSITORY) $(CI_PATH);
-include $(MAKEFILE)
