.PHONY: notebook docs
.EXPORT_ALL_VARIABLES:

install: 
	@echo "Installing project dependencies with Poetry..."
	poetry install

activate:
	@echo "Activating Poetry Virtual Environment"
	poetry shell

initialize_git:
	git init 

setup: initialize_git install

## Delete all compiled Python files
clean:
	find . -type f -name "*.py[co]" -delete
	find . -type d -name "__pycache__" -delete
	rm -rf .pytest_cache