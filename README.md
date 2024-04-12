# Design and Development of a Mouse Gene family database
## Background
Gene families refer to a group of genes that share similar sequences and functions, typically evolving from a common ancestral gene. Members within a gene family are referred to as homologous genes. Based on the manner in which they arise, they can be further classified into orthologous genes and paralogous genes. Orthologous genes arise through speciation events, while paralogous genes are generated through gene duplication (Figure 1). Members of gene families often retain some common structures or functions, but they may also undergo differentiation and specialization to adapt to various biological functions and environmental requirements.  

The significance of gene families lies in providing crucial insights into the process of evolution. By comparing the sequences and functional changes among different members of gene families, scientists can understand the genomic evolutionary processes involved in adaptation to diverse environments and functions. Additionally, gene families may play important roles during evolution, such as providing new functions, increasing genomic diversity, and facilitating genetic variation.  

Annotation of gene families requires extensive manual effort, making a high-quality gene family annotation database invaluable. For instance, HGNC (Human Gene Nomenclature Committee) provides the most comprehensive annotation for human gene families. However, in specific animal experiments, mice are common model organisms, and their database, MGI (Mouse Genome Informatics), still lacks adequate annotation for gene families. For example, MGI's annotation of paralogous genes significantly lags behind that of orthologous genes between different species.   

Therefore, I aim to develop a mouse gene family database by mapping corresponding gene family data from humans to mice. This endeavor will greatly facilitate background understanding, target selection, and result interpretation in mouse experiments.  

## Functionality
The human gene family data from HGNC (https://www.genenames.org) and the Mouse Genes with Alliance Homology and HGNC IDs data from MGI (https://www.informatics.jax.org) are two main data sources we used in this project. By mapping them together through HGNC id, we could design a schema of the mouse gene family database and the website. The website would display two gene families’ information in one page by default and you can switch the page to browse them. The information would include gene symbol, gene name, MGI id, HGNC id, chromosome, family name, family id, etc. The website would also allow users to input the keywords to search for specific gene families they are interested in.    

## Description
To achieve this goal, the mouse gene family database may utilize the following software technologies to carry out its functionality (Figure 2):

**HTML/CSS/JAVA -**  Provides a simple, user-friendly and interactive user interface for user’s input and visualization of the output after backend data generation. A HTML script to display the results on websites, probably a CSS script to modify the style and a JAVA script to add some useful interacting functions.  

**CGI -** Receives the input from users and interacts with the MYSQL database to retrieve the corresponding results.  

**SQL -** Stores the mouse gene family database and provide the necessary data for CGI script. It would consist of five tables: Gene family, human gene, mouse gene, homologous gene pairs and gene family members (Figure 3).  
