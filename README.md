# ChemSearch
ChemSearch. is a software tool that leverages the GSSDH graph similarity search algorithm to identify compounds in a database that are similar to a given query compound.

## Environment
ChemSearch requires a machine with 64-bit Linux. Ensure that the `./ChemSearch` binary is available and executable in your working directory.

## Installation
Clone the repository:
```sh
git clone https://github.com/SNUCSE-CTA/ChemSearch.git
cd ChemSearch
```
Ensure the `./ChemSearch` binary is compiled and executable:
```sh
chmod +x ./ChemSearch
```

## Usage
```sh
./ChemSearch -d [database] -q [chemical compound] -t [threshold]
```

### Arguments
 - `-d`: Path to the compound database file.
 - `-q`: Path to the query compound file.
 - `-t`: Threshold for the Graph Edit Distance.

### Output
 - Lists the IDs of compounds in the database similar to the query compound.
 - The final line displays the total number of matching compounds.

## Example
### Input
```sh
./ChemSearch -d AIDS.database -q chem-654113.txt -t 5
```
### Output
```sh
Data Graph ID '625064'
Data Graph ID '654113'
Data Graph ID '654114'
Data Graph ID '665553'
Number of Data Graphs with GED(q, G) ≤ τ : 4
```

## License
Distributed under Apache License 2.0. See LICENSE for more information.
