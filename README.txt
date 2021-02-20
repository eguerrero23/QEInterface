How to use
-----------
Compatible with Quantum ESPRESSO v6.0

Open this file and Evaluate All using Mathematica

To query a function's usage, Run ?FUNCTIONNAME

------------------------------
Basic usage:

var = QEImport[listOfFiles, typeOfCalculation]

* var will be the variable that holds all of the parsed output as 
	an Association
	* It is useful to use Keys[var] to check for available output
	* var will be initially empty, but will be built as functions
		are used on vars. (e.g. var[["energy"]] appears after
		running ShowEnergies[var])

* listOfFiles is a list of strings that are the filenames (e.g. 
	{"qe1.scf.out", "qe2.scf.out", "qe3.scf.out"}) of the QE output
	* If there is only one file, you need to make a list of one
		file, i.e. {"fileName"}, as the variable

* typeOfCalculation can be "scf", "relax", or "vc-relax"

------------------------------
To calculate the energy and parse energy-related information, use
ShowEnergies[var]

------------------------------
To see the structure and parse structure-related information, use
ShowStructure[var]

(currently only supports vc-relax)

------------------------------
To compute the kinetic energy cutoff analysis, upload a list of
scf files. Then use
ShowKineticEnergyCutoff[var]