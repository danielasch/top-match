+-------------------------------------------------------+
|						Top-match                      	|
|														|
|        		Command Line Interface version          |
|        		Copyright								|  
|														|
|	This product includes software developed at PUCRS  	|
|	by the NLP team 									|
|	(http://www.inf.pucrs.br/linatural/wordpress/).		|
|														|
+-------------------------------------------------------+
|				About Top-match							|
|														|
|	Top-match is an ontology matching system that 		|
|	generates alignments between top ontologies 		|
|	(DOLCE, SUMO and DUL) and any domain ontology. 		|
|   													|
|	If you use top-match, please cite the following		|
|	publication:										|
|														|
|	For more information, read:							|
|		- D. Schmidt, R. Basso, C. Trojahn, R. Vieira.	| 
|		"Matching domain and top-level ontologies via	| 
|		OntoWordNet", International Workshop on OM,		|
|		2017. (english)									|
|		- R. Basso, D. Schmidt, C. Trojahn, R. Vieira.	|
|		"Top-level and Domain ontology Alignment via 	|
|		WordNet", IX Seminar on Ontology Research in 	|
|		Brazil, 2017. (BR-portuguese)					|
+-------------------------------------------------------+
|				System Requirements						|
|														|
|	Top-match requires Java SE Runtime Environmet 8+.	|
|														|
|	CPU: Intel Core i5-2400 @ 3.10GHz or better			|
|	Memory: 4GB RAM or higher							|
|		Keep in mind that memory usage depends on the 	|
|		size of the ontologies. Therefore, opening 		|
|		large ontologies may take a while. 				|
+-------------------------------------------------------+
|				Top-match CLI Usage						|
|														|
|	Running top-match through the command line:			|
|														|
|	Access the top-match.jar folder and type:			|
|														|
|	$~java -jar top-match.jar [PARAMETERS]				|
|														|
|	The parameters order are:							|
|														|
|	-[domain ontology path]								|
|		ex: C:/Users/.../ontology.owl					|
|	-[rdf alignment path] (to be generated)				|
|		ex: C:/Users/.../alignment.rdf					|
|	-[top ontology] (dolce, sumo or dul)				|
|		ex: dolce										|
|	-[alignment technique] (0, 1, 2 or 3)				|
|		ex: 2											|
|	-[reference alignment path] OPTIONAL				|
|		ex: C:/Users/.../referenceAlign.rdf				|
|														|
|	Examples:											|
|														|
|	a) Use top-match to align a domain ontology with 	|
|	dolce, sumo or dul:									|
|	$~java -jar top-match.jar C:/Users/.../ontology.owl |
|	C:/Users/.../alignment.rdf sumo 2					|
|														|
|	b) Use top-match to align a domain ontology with	|
|	dolce, sumo or dul and evaluate the genereted		| 
|	alignment with a reference alignment:				|
|	$~java -jar top-match.jar C:/Users/.../ontology.owl |
|	C:/Users/.../alignment.rdf sumo 2 					|
|	C:/Users/.../refAlign.rdf							|
+-------------------------------------------------------+
|				About Techniques						|
|														|
|	These techniques modify the synset disambiguation	|
|	method.												|
|														|
|	1 -> Based on lesk word sense disambiguation:		|
|		Overlaps the context with the bag of words of	|
|		a synset. 										|
|	2 -> Word Embedding disambiguation:					|
|		Uses the average cossine distance between the	|
|		context and the bag of words of a synset.		|
|	3 -> Developing										|
+-------------------------------------------------------+