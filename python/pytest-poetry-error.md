# Error running pytest on python 3.10 in poetry project

Was getting the following error: `TypeError: required field "lineno" missing from alias` when trying to run pytest
This is because the version of pytest that is installed with poettry is old. You neeed to remove and then reinstall
the version of pytest

`poetry remove --dev pytest && poetry add --dev pytest`

[Source](https://stackoverflow.com/questions/69528842/an-error-while-trying-to-execute-tests-on-python-3-10-with-pytest)
