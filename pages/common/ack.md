# ack

> A search tool like grep, optimized for programmers. - By default ack is recursive

- do a case case-insensitive search with: 

`ack -i "some.dude@somedude.com" `

- search for string ignoring yml file extension:

`ack --ignore-file=ext:yml "{{search_string}}"`

- Find files in a specific language:

`ack --ruby {{each_with_object}}`

- Count the total number of matches for the term "foo":

`ack -ch {{foo}}`

- Show the file names containing "foo" and number of matches in each file:

`ack -cl {{foo}}`
