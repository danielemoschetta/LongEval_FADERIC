# FADERIC - LongEval CLEF 2023 Lab, Task 1. LongEval-Retrieval

Project of group FADERIC submitted to the LongEval Lab at CLEF 2023, Task 1 - LongEval-Retrieval (https://clef-longeval-2023.github.io/). 

The projects consists of a search engine designed to mantain performace over time, therefore the system has been evaluated using different document collections, acquired at different times.

The system has been devloped in Java 17 using Apache Lucene (https://lucene.apache.org/) and its main features are:

* Analyzer using tokenizing, stopword removal, stemming;
* Searcher using word n-grams, fuzzyness, query expansion with synonyms also exploiting Apache OpenNLP (https://opennlp.apache.org/);
* Document reranking using a BERT model trained on the MS-MARCO dataset (https://huggingface.co/Luyu/bert-base-mdoc-bm25) and the pytorch (https://pytorch.org/) and pygaggle (https://github.com/castorini/pygaggle) libraries.

## Results ##

The submitted system has achieved the best overall performance among the submitted systems, according to the overview and results available at https://ceur-ws.org/Vol-3497/paper-184.pdf.

The paper describing the project is available at https://ceur-ws.org/Vol-3497/paper-188.pdf. 

## Instructions ##

To reproduce the runs you can set the preferred properties in the configuration file `src/main/resources/config.xml` and run the project using Apache Maven (https://maven.apache.org/).

To use the reranking feature you have to follow these instructions:

* Install Microsoft Visual C++ 14.0 (or greater), you can get it with Microsoft C++ Build Tools at https://visualstudio.microsoft.com/visual-cpp-build-tools/ 
* Install Python v3.7.9
* Add the installation directory to the `PATH` environment variable, it has to be the first Python directory to appear in the list otherwise the other one will be chosen
* Set the `PYTHONHOME` environment variable to the installation directory
* Install the following packages in Python v3.7.9: 
    * jep v4.1.1
    * pygaggle v0.0.3.1
    * torch v1.5.0, please follow the right install options for your machine available at https://pytorch.org/get-started/previous-versions/#wheel-17
