WikiIndexer
===========
 <pre>
 Steps to set-up the program. These steps are provided with eclipse as envirionment.
	->Download the Zip file to your local system
	->Extract it.
	->Open Eclipse-Import-> Import Exisitng project
	->Click Browse and select the root folder(WikiIndexer) 
	->Click Next/Finish
 Run the project. It should execute.
 Main method is in edu.buffalo.cse.ir.wikiindexer.SingleRunner.java.(Starting point)
 By default, this program takes five_entries.xml as input file. This file is present in "files" folder. 
 In case user want to parse his/her own wikipedia xml file or make it configurable, user has to do two configuration changes.
	1. Add the xml file to files/properties.config. Currently it is set to as follows;
		root.dir=/home/rahul/Desktop/WikiIndexer(path)
		dump.filename=five_entries.xml(filename)
	2. Run the program with two runtime arguments. Set the runtime arguments in eclipse.
		1. path of the properties file.It is present in "files" folder.
		2. mode. (There are two modes -i and -t)
Description:
===================
 This project takes the wikipedia xml file as input.It consist of wikipedia articles/pages/document.
 It cleans & parses the content which means remove the wiki markup.(Check http://en.wikipedia.org/wiki/Help:Wiki_markup <br/> for details on   wikimarkup)
 Tokenize the content.
	For Example: Input-> This is a Wikipedia page on scandals.
		     Output-> This, is, a, Wikipedia, page, on, scandals
 Stop words are removed.
		     Output-> Wikipedia, page, scandals
 Index the wikipedia pages based on tokens. Imagine it as table with two columns "tokens" and "document Id".

Usage:
==================
This program can be used in developing a search Engine. Whenever user types in query say "scandals". it looks into the <br/> index files and return the document id. and corresponding document can be displayed.
</pre>
