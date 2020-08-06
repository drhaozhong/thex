# Which Exception Shall Be Thrown?

## Project summary

When a runtime error occurs, in many programming languages, programmers can throw an exception. A thrown exception can be caught and handled afterwards. Although the process is critical to resolve runtime errors, it can introduce bugs and lead to disastrous consequences. The state-of-the-art research focuses on the bugs in catching and handling exceptions. For example, after an exception is thrown from a code line, its follow-up lines are bypassed. As a result, some resources are not closed. The prior tools can detect and fix such bugs. 

In this paper, we argue that a thrown exception can be also buggy. For example, when a type of runtime errors occur, an incorrect exception can be thrown. When this happen, the thrown exception can never be caught and handled. Although thrown exceptions can be buggy, to the best of our knowledge, no approach can detect such bugs, because exceptions are many and the rules of throwing exceptions are complicated. 

In this project, for the first time, we propose an approach to predict which exceptions shall be thrown under a given programming context. Its basic idea is to learn a classification model from the features that were extracted from thrown locations. 


## Our extracted features

We used our tool to extract the features from nine projects, and dumped them into the arff files of weka. These files are uploaded: 
[asm](https://github.com/ackelcn/activemq), [commons-io](https://github.com/ackelcn/aries), [itext](https://github.com/ackelcn/carbondata), [jfreechart](https://github.com/ackelcn/cassandra), [jmonkey](https://github.com/ackelcn/derby), [lucene](https://github.com/ackelcn/mahout), [pdfbox](https://github.com/ackelcn/uima-uimaj), [poi](https://github.com/ackelcn/uima-uimaj), and [shiiro](https://github.com/ackelcn/uima-uimaj).


Weka can be downloaded from its [website](http://www.cs.waikato.ac.nz/ml/weka/). It can read our dumped arff files and train models based on our data. 


