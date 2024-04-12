# Design and Development of a Mouse Gene family database
## Background
Gene families refer to a group of genes that share similar sequences and functions, typically evolving from a common ancestral gene. Members within a gene family are referred to as homologous genes. Based on the manner in which they arise, they can be further classified into orthologous genes and paralogous genes. Orthologous genes arise through speciation events, while paralogous genes are generated through gene duplication (Figure 1). Members of gene families often retain some common structures or functions, but they may also undergo differentiation and specialization to adapt to various biological functions and environmental requirements.  

BLAST might be the most well known one among all the MSA tools. In this case, all I want to do is to reproduce a classic mutiple sequence alignment tool website just like BLAST. However, allowing for the fact that the server memory might be limited, the tool can only be used to achieve the sequence vs sequence alignment rather than the sequence vs database analysis.  
## Functionality
This MSA tool requires the user to input a fasta format file which should contain two sequences at least. The '>' annotation line shouldn't be eliminated. There would also include some basic parameters such as selecting the calculation method, the gap costs and so on.  

The output would display the alignment result, score and p-value of all sequences.
## Description
To achieve this goal, the MSA tool may utilize the following software technologies to carry out its functionality:

**HTML/CSS/JAVA -**  provides a simple, user-friendly	and	interactive	user interface for user’s input and visualization of the output after	backend	data generation. 
a cgi script to conduct the sequence alignment in the server, a mysql database to store the results and probably a css script to modify the style.

**CGI -** carries out the logical calculation of the alignment on the server, which requires the installation and use of biopython package. The script would receive the input from the html and pass it to the commands to get the result.

**SQL -** keeps the input history.
