# Leak report

The problem was that result in strip (line 47) was allocated memory with calloc, and never freed it.
To fix this simply write free(result) after everything else in the funtion but before the return 
statement.
