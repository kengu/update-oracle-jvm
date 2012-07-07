#
# This makefile compiles the project listed in the PROJ macro
#
PROJ = update-oracle-jvm	# the name of the project
OBJS = *			# folder with source files
COND = conf.d			# folder with configuration files
CONF = config			# configuration file
EXCL = *~			# excluded files

#
# Configuration
#
#SHELL := /bin/bash

#
# Run all commands
#
all: clean build package 

#
# Clean previous builds
#
clean:
	@echo 
	@echo --------------------------------------------------------
	@echo Cleaning previous builds...
	@echo --------------------------------------------------------
	@if [ "$(version)" = "" ]; \
		then for f in $(strip $(PROJ))-*; do if [ -d $$f ]; then rm -R $$f; echo Removed build $$f; fi; done; \
	 	elif [ -d $(strip $(PROJ))-$(version) ]; then rm -R $(strip $(PROJ))-$(version); echo Removed build $(strip $(PROJ))-$(version); fi;
	@echo Clean: completed

#
# Build version
#
build : clean
	@echo 
	@echo --------------------------------------------------------
	@echo Building version $(version)...
	@echo --------------------------------------------------------
	@if [ "$(version)" = "" ]; then echo Version is missing, execute \'"make" build version=...\'; exit 1; fi
	@mkdir $(strip $(PROJ))-$(version)
	@cp -R ../src $(strip $(PROJ))-$(version)
	@cp installer $(strip $(PROJ))-$(version)/src
	@cd $(strip $(PROJ))-$(version)/src; tar -zcvf ../$(strip $(PROJ)).tar.gz $(strip $(OBJS)) --exclude=$(strip $(EXCL)) --exclude=$(strip $(COND))/$(strip $(CONF)) --exclude=$(strip $(COND))/$(strip $(EXCL));
	@echo Build $(strip $(PROJ))-$(version): completed

#
# Build Self-extracting script (see http://www.linuxjournal.com/node/1005818)
#
package : 
	@if [ ! -d $(strip $(PROJ))-$(version) ]; then make build version=$(version); fi
	@echo 
	@echo --------------------------------------------------------
	@echo Building self-extracting package...
	@echo --------------------------------------------------------
	@if [ "$(version)" = "" ]; then echo Version is missing, execute \'"make" package version=...\'; exit 1; fi
	@cd $(strip $(PROJ))-$(version); cat ../extractor $(strip $(PROJ)).tar.gz > $(strip $(PROJ))-$(version).bin; chmod +x $(strip $(PROJ))-$(version).bin 
	@echo Package $(strip $(PROJ))-$(version): completed



