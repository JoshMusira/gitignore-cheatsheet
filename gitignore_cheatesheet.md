| PATTERN | EXPLANATION | EXAMPLES |
| --------|---------|---------|
| **/logs | You can prepend a pattern with a double asterisk to match directories anywhere in the repository. | logs/debug.log |
| **/logs/debug.log | You can also use a double asterisk to match files based on their name and the name of their parent directory. | logs debug.log|
| *.log | An asterisk is a wildcard that matches zero or more characters | foo.log |
| *.log !important.log | Prepending an exclamation mark to a pattern negates it. If a file matches a pattern, but also matches a negating pattern defined later in the file, it will not be ignored | trace.log |
| *.log !important/*.log trace.* | Patterns defined after a negating pattern will re-ignore any previously negated files | debug.log |
| /debug.log | Prepending a slash matches files only in the repository root | debug.log |
| debug.log | By default, patterns match files  in any directory | logs/debug.log |
| debug?.log | A question mark matches exactly one character | debug0.log |
| debug[0-9].log | Square brackets can also be used to match a single character from a specified range | debug1.log |
| debug[01].log | Square brackets match a single character  form the specified set. | debug0.log |

