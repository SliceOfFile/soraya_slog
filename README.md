# soraya_slog

soraya_slog is a simple Python structured logging library that writes
JSON-formatted output to stdout. The output format is compatible with
that defined for [Google Cloud Logging](log-format). The library is
designed to be used with projects related to Soraya, an experiment in
conversational AI that can be found at the [SliceOfFile](slice-of-file)
GitHub organization.

## Installation

soraya_slog can be installed using pip:

```bash
pip install soraya-slog
```

## Usage

Using soraya_slog is very simple. You just need to import the library
and call the log method with the message, severity level and additional
data. The severity levels are compatible with those for Google Cloud
Logging, and are as follows:

- `DEBUG`
- `INFO`
- `NOTICE`
- `WARNING`
- `ERROR`
- `CRITICAL`
- `ALERT`
- `EMERGENCY`

Here's an example.

```python
import soraya_slog
soraya_slog.log('ERROR', 'This is an error message', { 'additional': 'data' })
```

You might also prefer to use any of the convenient methods available for
each severity level, such as in the following example.

```python
import soraya_slog
soraya_slog.error('This is an error message', { 'additional': 'data' })
```

## License

soraya_slog is licensed under The Unlicense. See the LICENSE file for
more information.

[log-format]: https://cloud.google.com/logging/docs/reference/v2/rest/v2/LogEntry
[slice-of-file]: https://github.com/SliceOfFile