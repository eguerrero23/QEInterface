How to use
-----------
Compatible with Quantum ESPRESSO v6.0

Open this file and Evaluate All using Mathematica

Run 
var = QEImport[listOfFiles, typeOfCalculation]

* var will be the new variable that holds all of the parsed output
* listOfFiles is a list of strings that are the filenames of the QE
	output. If there is only one file, you need to make a list
	of one file, i.e. {"fileName"}, as the variable
* typeOfCalculation can be either "scf" or "vc-relax" currently

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