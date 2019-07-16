# pytest (Python ) Cheatsheet

## Commands
- `@pytest.fixture(autouse=True)` each pytest test will be sandwiched into this function. It's run once per test, doing all its setup and teardown each time.

## Options
- `-l/--show-locals` shows local variables if a test fails
- `--lf/--last-failed` runs tests, starting with the last one that failed.
- ``

## Markers
- `@pytest.mark.xfail` - we expect this test to fail