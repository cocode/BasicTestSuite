# <img src="images/BasicTestSuite.png" alt="Logo" width="50" height="25"> BASIC Test Suite

This is a collection of BASIC programs that will exercise various features of the langauge.


This is is part of the TrekBasic family of BASIC programming tools.
* [TrekBasic](https://github.com/cocode/TrekBASIC) - Python version
* [TrekBasicJ](https://github.com/cocode/TrekBasicJ) - Java Version
* [BasicRS](https://github.com/cocode/BasicRS) - Rust version
* [BasicTestSuite](https://github.com/cocode/BasicTestSuite) - A test suite of BASIC Programs
* [TrekBot](https://github.com/cocode/TrekBot) - A tool to exercise the superstartrek program

The Basic Test Suite  is used by TrekBasic, TrekBasicJ and BasicRS, three implementations of BASIC that we have implemental. All of those projects are committed to supporting exactly the same langauge, and this suite is used to verify that. 

Test runners (in Python, Java and Rust) simply iterate over all *.bas files found in the directory. Those test runners are found in their respective projects, above.

## Conventions

The test programs are supposed to run and return a 0 (success) status code. 

## Directives

### EXPECT_EXIT_CODE

The test runners chack the first line for a rem statement with directives. A STOP would normally indicate an error, but with EXPECT_EXIT_CODE=1, exiting with 1 (STOP) 
is considered success.

100 REM @EXPECT_EXIT_CODE=1

This indicates that a program should finish with a STOP command, which would normally be an error.



