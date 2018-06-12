# find

> Find files under the given directory tree, recursively.

- Find files by extension:

`find {{root_path}} -name '{{*.ext}}'`

- Find files matching path pattern:

`find {{root_path}} -path '{{**/lib/**/*.ext}}'`

- Run a command for each file, use {} within the command to access the filename:

`find {{root_path}} -name '{{*.ext}}' -exec {{wc -l {} }}\;`

- Find files that are not within a .git folder and then replace string with other_string, in the CWD:

`find . -not -path '*/\.git*' -type f -exec sed -i 's/{{string}}/{{other_string}}/g' {} +`

- Find files created in the last 30 minutes:

`find . -cmin -30`

- Find files modifed in the last 30 minutes:

`find . -mmin -30`

- Find files modified in the last 24-hour period:

`find {{root_path}} -mtime {{-1}}`

- Find files matching a given pattern, while excluding specific paths:

`find {{root_path}} -name '{{*.py}}' -not -path '{{*/site-packages/*}}'`
