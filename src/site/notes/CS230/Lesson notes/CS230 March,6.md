---
{"dg-publish":true,"permalink":"/cs-230/lesson-notes/cs-230-march-6/"}
---

*read the [Coding Standards](https://docs.google.com/document/u/1/d/1f3E1WRj6JHMvg-k_31sZLxFy1Ab9_2YHObhy7lY8u18/edit)*

*debugger, logging service*

[Tutorial 1.1](https://docs.google.com/presentation/u/1/d/1hQpml0MXjlow-O_zhx6wyrW924YyMdekl9WQZ9Mob9o/edit) this is a homework assignment march 16!!

> [!HOMEWORK]
> - [ ] Write the logic that will be inside of CS230::Logger::log() that does not use if/else statements
> - [ ] Use out_stream << message to print the message
> - [ ] include the severity level of the message being printed. (“Verbose,” “Debug,” “Error,” or “Event”) Also include a tabspace character. (“\t”)
> - [ ] Remember to check min_level to determine if the message should output.
> - [ ] EXTRA CREDIT - Dont use a switch statement and use only one if statement.


> *You don’t need to know how out_stream.set_rdbuf() works, just know that it will set out_stream to write to “Trace.log” if use_console is set to true whenever you use something like out_stream << “Hello!” .*
> *By default, Raylib will output a lot of stuff into the console window. Using SetTraceLogLevel(), we can hide it.*


