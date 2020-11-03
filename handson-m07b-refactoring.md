---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
# Hands-On Exercise 7b & 7c: Refactoring

## Goals
Exercise 7b: Refactoring the code to enable addition of new integration methods without having to modify the source code.
Exercise 7c: Refactor a poorly structured code to a cleaner, more reusable version.

## Prerequisites
* A [GitHub](https://github.com) account
* A fork of the [betterscientificsoftware/hello-numerical-world-sc20](https://github.com/betterscientificsoftware/hello-numerical-world-sc20) repository in your account (covered in exercise 3)
* Access to a basic software development environment for C++ languge
   - Your fork of the tutorial repository should be cloned in this working environment (covered in exercise 3)

## Background
In Module 7 of the tutorial presentations, we discuss the refactoring process. In the first exercise you are given a modular well written code that supports multiple integration methods, your task is to refactor is so that another integration method can be added without having to modify the source code in future. 

In the second exercise, your task will be to refactor the code you've inherited.  Exercise 7a is a planning activity for this work, which uses the epic-story-task model with GitHub issues and a project board.  You are encouraged to work through 7a and this exercise in tandem, or to complete 7a first.

You've inherited the heat equation example code `heatAll.C` from a colleague who's left your project.  Your task is to refactor it to make it cleaner and more reusable.

*Note: the code used in exercise 1 is a possible solution for exercise 2, but it is not a unique solution -- yours may be different.*

## Instructions for exercise 1

The code currently has three different finite-difference schemes to update the solution to the heat equation: `crankn` (Crank-Nicolson), `ftcs` (forward-time central-space), and `upwind15` (upwind).  We'd like the code to be more flexible so that other approaches can be added to update the solution without having to modify the main heat equation driver every time.  More specifically, the `update_solution` interface needs to be generalized. 

Relevant files in this exercise are: 
Header files -- Double.H	heat.H	
Source files --  args.C		crankn.C	exact.C		ftcs.C		heat.C		upwind15.C	utils.C
Build file -- makefile

All refactoring exercises should begin by checking the test coverage for the part of the code you'll be working on and gathering baseline results with the original code.

1. In your working copy of the repository, in the `makefile`, add the `-coverage` flag to the rules to generate object files and to link the final `heat` application.
```
# Implicit rule for object files
%.o : %.C
	$(CXX) -coverage -c $(CXXFLAGS) $(CPPFLAGS) $< -o $@

# Linking the final heat app
heat: $(OBJ)
	$(CXX) -coverage -o heat $(OBJ) $(LDFLAGS) -lm
```
then build the `heat` application by typing  `make`.

2. Run
```
./heat runame="ftcs_results"
gcov heat.C
cp heat.C.gcov heat-ftcs.C.gcov
```
and examine the resulting `heat-ftcs.C.gcov` file.  The output of gcov is a listing of the code annotated on the left with the following notations:
- a dash indicates a non-executable line, 
- a number indicates the number of time the line was executed, and 
- hash marks ("#####") indicate that the line was *never* exercised.
You'll notice that the calls to the `update_solution_upwind15` and `update_solution_crankn` routines were never exercised.

3. Collect coverage and baseline results for the other update schemes.
```
./heat alg="upwind15" runame="upwind_results"
gcov heat.C
cp heat.C.gcov heat-upwind15.C.gcov

./heat alg="crankn" runame="crankn_results"
gcov heat.C
cp heat.C.gcov heat-crankn.C.gcov
```
Compare the three gcov output to ensure that between the three test cases you've run, you have good coverage for the regions of code on which you're going to work.



Refactoring – The starting code 
Interfaces are not identical
crankn  has an extra argument
It also has an extra step in initialization

Refactoring 
Generalize the interface
Modify the makefile

Add null implementations of initialize_crank in ftcs and upwind15

make heat1
Run ./heat runame=“ftcs_results”
Make heat2
Run ./heat runame=“upwind_results”
Verify against baseline

## Instructions for exercise 2

1. Create a new directory and copy the original makefile from exercise 1, and heatAll.C into the new directory. This will be your working area. Work in tandem with exercise 7a to plan your work.

2. Compile heatAll.C with coverage flags enabled similar to exercise 1. Run the executable with various permutations of input arguments, saving each output as a baseline for comparison until you have 100% coverage.

3. Make a decision about how many files you wish to split the code into. A good rule of thumb is to start with a different file for each category of functions. An example would be to create integrate.C, a utils.C and a main.C to which you copy from heatAll.C functions that belong in each category. 

4. Make a decision about which variable and constants you wish to have available globally and which you wish to keep local. Create ".H" files for global variables.

5. In each of the new ".C" file add "extern" interfaces for functions that are not in the same file, and "include" statements for any header files you might wish to include. 

6. In the makefile replace existing filenames with the ones you have just created. 

7. Compile and execute the refactored code in all permutations used in step 2 and verify against the corresponding baselines.

8. If you are happy with the modularity of your refactored code you are done. If you wish to further modularize repeat steps 3-7 until you have the reached your refactoring objectives.




