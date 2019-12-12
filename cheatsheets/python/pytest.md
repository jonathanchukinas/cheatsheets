# pytest (Python ) Cheatsheet

## Existing Cheatsheets:
- https://gist.github.com/kwmiebach/3fd49612ef7a52b5ce3a

## Commands
- `@pytest.fixture(autouse=True)` each pytest test will be sandwiched into this function. It's run once per test, doing all its setup and teardown each time.

## Options
- `-l/--show-locals` shows local variables if a test fails
- `--lf/--last-failed` runs only those tests that last failed
- `-v` verbose mode
- `-k` filter on test function name
- `-m` filter on pytest marks

## Markers
- `@pytest.mark.xfail` - we expect this test to fail

## pytest-cov
- `pytest --cov=myproj tests/`
- `pytest --cov-report term-missing --cov=myproj tests/`
