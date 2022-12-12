# retrieval-project
OOD3
Class CLI
Attributes
•	boolean isDebug - the debug flag
Services
•	void process() – return nothing but executes commands
•*/* purpose: process args input and search files for query
•* input: String [] args - the command line input
•* query - the input to search for
•* results: created stoplist and inverted index to search through
•**/
•	void usage() – print usage message if args is not correctly inputted
•*/* purpose: print usage message and stop program if args is not correctly inputted
•* input: na
•* results: usage message and end program
•**/

Class Index
Attributes
•	HashMap<String, HashSet<File>> invertedIndex – the inverted index used by the search engine 
Services
•	Index() - create new empty invertedIndex
•*/* purpose: create a new empty index
•* input: na
•* results: new index
•**/
•	void buildIndex() – return inverted index as Hash with scanned document words as keys and set of matching documents as value
•*/* purpose: return inverted index as Hash with scanned document words as keys and set of matching documents as value
•* input: String docName - the name of the file to open and inverse index
•* HashSet<String> stoplist - the set of words to ignore when indexing
•* results: updated inverted index
•**/

Class Search
Attributes
•	String query – the word(s) to find
•	HashMap<String, HashSet<File>> invertedIndex – the inverted index the search looks at
•	HashSet<File> docList - the set of files to find and return
• HashSet<String> strings - the names of the matching documents
Services
•	Search() - return set and number of files that match all query word(s)
•*/* purpose: return and print inverted index as HashSet with scanned document words as keys and set of matching documents as value
•* input: String query - the word(s) to find
•* HashMap<String, HashSet<File>> invIndex - the inverted index to search through
•* boolean isDebug - the debug flag
•* results: updated inverted index
•**/
• String stripFiles() - return file name from given file path
•*/* purpose: strips given filepath to return filename
•* input: File f, the filepath to be stripped
•* results: stripped filename
•**/ 
• void debugFunction() - prints names and contents of matching files if debug flag is true
•*/* purpose: prints names and contents of matching files if debug flag is true
•* input: HashSet<File> docs - the set of docs to print paths and contents
•* results: printed paths and contents of matching docs
•**/

Class Stoplist
Attributes
• HashSet<String> stoplist - the set of words to ignore
Services
• Stoplist() - return new empty stoplist
•*/* purpose: create a new empty stoplist
•* input: na
•* results: new stoplist
•**/
• buildStoplist() - return stoplist created from stoplist file
•*/* purpose: fill a stoplist with words from stoplist file
•* input: String stoplistStr - the name of the stoplist
•* results: updated stoplist
•**/

Class StringReader
Attributes
Services
•	StringReader() - return new constructor for iterator
•*/* purpose: create a new string reader constructor
•* input: String s - the String to pass to the iterator
•* results: new constructor
•**/
•	Iterator<String> iterator - returns string as iterable tokens stripped of ignored characters
•*/* purpose: create a string as iterable tokens stripped of ignored characters
•* input: na
•* results: iterable string without ignored characters
•**/
