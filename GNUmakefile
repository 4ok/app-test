### SETTINGS
### ========

# Project root path
ROOT_PATH := $(PWD)

# Node modules bin path
NODE_MODULES_BIN_PATH := $(ROOT_PATH)/node_modules/.bin

# BEM path
BEM_PATH := $(ROOT_PATH)/bem

### LINT
### ====

# Lint stylus, js files
.PHONY: lint
lint: lint.stylus lint.js

.PHONY: lint.stylus
lint.stylus:
	@echo '===> Linting stylus files'
	$(NODE_MODULES_BIN_PATH)/stylint --config $(NODE_MODULES_PATH)/stylint-config-4ok/.configrc $(BEM_PATH)/blocks/

.PHONY: lint.js
lint.js:
	@echo '===> Linting js files'
	$(NODE_MODULES_BIN_PATH)/eslint .
