# sqlpp-experiments

* sqlpp-experiments is a base of sqlpp(11) examples

* Done by Eloi du Bois

* LICENSE: LGPLv3

## Compilation

To compile, you will need boost and scons:

* boost: (http://www.boost.org/users/download/)
* scons: (http://www.scons.org/)

First, clone the repository:

```
git clone https://github.com/edubois/sqlpp-experiments.git
cd sqlpp-experiments
git submodule update -i
```

This should bring tools/sconsProject

now, go into tools/sconsProject


Now, it's time to edit default.sconf according to your configuration.
In the default configuration, I made a parent directory 3rdParties where I put
my 3rd party libraries. To change your external libraries base dir, 
edit the variable extern in this file (default.sconf).
If you are using Mac, adapt the last lines according to your
XCode configuration.
If you are not using Mac, remove the lines after '# Mac only'

When you are ready, enter:

scons mode=release

This will build the default example application.


## Examples

Please note that ```scons example_name``` will build the example in question

* debtsReminder

This is an example of debts booking and reminder software using a database by means of sqlpp11.


