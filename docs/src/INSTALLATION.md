# cmdstan installation

## Minimal requirement

Note: CmdStan.jl and CmdStan refer this Julia package. The executable C++ program is 'cmdstan'.

To run this version of the CmdStan.jl package on your local machine, it assumes that the  [cmdstan](http://mc-stan.org/interfaces/cmdstan) executable is properly installed.

In order for CmdStan.jl to find the cmdstan you need to set the environment variable `JULIA_CMDSTAN_HOME` to point to the cmdstan directory, e.g. add

```
export JULIA_CMDSTAN_HOME=/Users/rob/Projects/Stan/cmdstan
launchctl setenv JULIA_CMDSTAN_HOME /Users/rob/Projects/Stan/cmdstan
```

to .bash_profile or config/startup.jl. I typically prefer cmdstan not to include the cmdstan version number so no update is needed when cmdstan is updated.

Currently tested with cmdstan 2.17.1

## Linux options

For those who are using a Linux based operating system. These are the cmdstan installation instructions using Linuxbrew. Please note that you must have Linuxbrew installed on your machine prior to going through these steps.

	Executing in a terminal:
	'''
	brew tap brewsci/science
	brew install cmdstan
	'''
	should install the latest available cmdstan in /home/usrname/.linuxbrew/Cellar/cmdstan/x.x.x:
	
Then set `JULIA_CMDSTAN_HOME` to point to where your local installation of cmdstan lives.

Note: Is this still valid?
