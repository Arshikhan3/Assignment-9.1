# Assignment-9.1
Q1.1. Why MapReduce program is needed in Pig Programming?
Ans: Pig is bit slower as compared to MapReduce as PIG commands are translated into MapReduce prior to execution that means 
Pig sits on the top of the existing infrastructure whatever we write in the pig or whatever we are developing in pig it gets converted ino mapreduce jobs and then we are able to execute it.

Q2. What are advantages of pig over MapReduce?
Ans: Pig is simple to learn and use as compared to Map Reduce.

An advantage PIG has over MapReduce is that the former is more concise. A 200 lines Java code written for MapReduce can be reduced to 10 lines of PIG code.
Mapreduce requires programmers most probably java programmers and programmers must think in terms of map and reduce functions.
Pig provides high level language that can be used by data analysts and data scientists.
Pig latin provides all of the standard data processing operations like oin, filter, group by, order by, union etc.

Q3. What is pig engine and what is its importance?
Ans: It acts as interpreter between pig latin script and mapreduce jobs. It creates environment to execute pig scripts into series of mapreduce jobs in parallel manner.

Q4. What are the modes of Pig execution?
Ans: We can run pig Apache in two modes.
1) Local Mode 
This mode is generally used for testing purpose. In this mode, all the files are installed and run from our local host and local file system. There is no need of Hadoop or HDFS.

2) MapReduce Mode
MapReduce mode is where we load or process the data that exists in the Hadoop File System (HDFS) using Apache Pig. In this mode, whenever we execute the Pig Latin statements to process the data, a MapReduce job is invoked in the back-end to perform a particular operation on the data that exists in the HDFS.

Q5. What is grunt shell in Pig?
Ans: The Grunt shell of Apache Pig is mainly used to write Pig Latin scripts. After invoking the Grunt shell, you can run your Pig scripts in the shell. In addition to that, there are certain useful shell and utility commands provided by the Grunt shell.
fs Command
Using the fs command, we can invoke any FsShell commands from the Grunt shell.
Syntax: grunt> sh File System command parameters

sh Command
Using sh command, we can invoke any shell commands from the Grunt shell. Using sh command from the Grunt shell, we cannot execute the commands that are a part of the shell environment (ex − cd).
Syntax: grunt> sh shell command parameters

Q6. What are the features of Pig Latin language?
Ans: Apache Pig is a high-level procedural language for querying large semi-structured datasets using
Hadoop and the MapReduce Platform.
Instead of providing Java Based API framework, Pig provides its own scripting language which is called as Pig Latin.
Pig Latin is a very simple scripting language. It has constructs which can be used to apply different transformation on the data one after another.
• Pig provides an engine for executing data flows in parallel on Hadoop. It includes a language, Pig
Latin, for expressing these data flows.
• Pig Latin includes operators for many of the traditional data operations (join, sort, filter, etc.), as
well as the ability for users to develop their own functions for reading, processing, and writing
data.

Q7. Is Pig latin commands case sensitive?
Ans: The names (aliases) of relations and fields are case sensitive. The names of Pig Latin functions are case sensitive. The names of parameters (see Parameter Substitution) and all other Pig Latin keywords are case insensitive.

Example:-
The names (aliases) of relations A, B, and C are case sensitive.
The names (aliases) of fields f1, f2, and f3 are case sensitive.
Function names PigStorage and COUNT are case sensitive.
Keywords LOAD, USING, AS, GROUP, BY, FOREACH, GENERATE, and DUMP are case insensitive. They can also be written as load, using, as, group, by, etc.
In the FOREACH statement, the field in relation B is referred to by positional notation ($0).
grunt> A = LOAD 'data' USING PigStorage() AS (f1:int, f2:int, f3:int);
grunt> B = GROUP A BY f1;
grunt> C = FOREACH B GENERATE COUNT ($0);
grunt> DUMP C;

Q8. What is a data flow language? 
Ans: In a dataflow language, you have a stream of data which is passed from instruction to instruction to be processed. Dataflow programs start with an input, perhaps the command line parameters, and illustrate how that data is used and modified.
Pig Latin shows users exactly the data flow, without forcing them to either think inside out or construct a set of temporary tables and manage how those tables are used between different SQL queries.This could be seen as data flowing through otherwise static instructions like how electrical signals flow through circuits or water flows through pipes.
