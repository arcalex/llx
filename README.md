llx
===

llx is a parallel execution shell.  It provides a simple way to process
an input list using a command template, maintaining a constant number of
processes running in parallel at any given time.  llx originally was a
script to parallelize the transfer of a large number of files and was
later generalized.  llx supports rerunning failed processes and timing
out on processes that exceed a user-defined threshold.

Try this simulation in bash(1):

```
while true; do echo $((RANDOM%8)); done | llx -v -n 4 -c 'sleep $1'
```
