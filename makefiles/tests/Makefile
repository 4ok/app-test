#
# Actions:
#
#    lint           Lint all files
#    lint.stylus    Lint stylus files
#    lint.js        Lint javascript files
#

########################################################
###                     Variables                    ###
########################################################

# Node modules directory
NODE_MODULES_DIR ?= node_modules

# Node modules binary directory
NODE_MODULES_BIN_DIR ?= $(NODE_MODULES_DIR)/.bin

# BEM path
BEM_PATH := bem

########################################################
###                     Functions                    ###
########################################################

#
# Print the title of action
#
# $(1) {String} Title
#
ifndef printActionTitle
define printActionTitle
    $(info )
    $(info =====> $(1))
endef
endif

########################################################
###                      Lint rules                  ###
########################################################

# Lint all files
.PHONY: lint
lint: lint.stylus lint.js

# Lint stylus files
.PHONY: lint.stylus
lint.stylus:
	$(call printActionTitle,Linting stylus files)

	$(NODE_MODULES_BIN_DIR)/stylint --config $(NODE_MODULES_DIR)/stylint-config-4ok/.configrc $(BEM_PATH)/blocks/

# Lint javascript files
.PHONY: lint.js
lint.js:
	$(call printActionTitle,Linting js files)

	$(NODE_MODULES_BIN_DIR)/eslint .
