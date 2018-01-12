## CheckMK Agent Listener

This is a simple python wrapper for checkmk_agent.  It provides CheckMK output without the need for xinetd.  It doesn't have access controls, so please only use it internally on secured networks.

If you can make improvements or enhancements, please make a pull request and submit your changes here.

# Files:
pycheckmk_agent.py:
- listens for a connection on port 6556
- forks a child process and sends node data to the port for CheckMK consumption
- closes the connection

pycheckmk_agent.service:
A systemD unit file for starting the pycheckmk_agent as a system service.