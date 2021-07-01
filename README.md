# regex_search
Python CLI tool similar to egrep but can return group matches

Created on Mon Oct 28 09:15:54 2019

@author: Henry James

Command line tool to search for regex per line and output results
whilst egrep has same functionality this tool will be able to
return regex groups allowing for great flexibility in the CLI.

Command use:
    regex_search.py [regex] [group number (default group 0)]

Examples where groups are useful

# returns the contents of anything matched between the OPERATION= and the ,
cat file | grep RULE:R | regex_search 'OPERATION=(.+?),' 1

# can search for multiples like this
cat file | grep CONDITION | head | regex_search 'GROUPNAME="(.+?)",RELATION=(.+?),' 1,2
