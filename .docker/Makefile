all: help

#.PHONY is used for run commands instead of files
.PHONY: help

t ?= models

ssh: ## ssh into app container
	docker exec -it php bash

up: ## docker up
	docker compose  up -d

down: ## docker down
	docker compose  down

ps: ## check if docker is up
	docker compose  ps

help:
	@grep -E '^[a-zA-Z0-9_-]+:.*?## .*$$' $(MAKEFILE_LIST) \
	| sed -n 's/^\(.*\): \(.*\)##\(.*\)/\1\3/p' \
	| column -t  -s ' '
