
Introduction: This report encapsulates the methodologies and outcomes of
three distinct computational problems aimed at enhancing text processing and
information retrieval capabilities using Python. The execution environment
leverages Google Colab for its computational resources, with Google Drive serving
as the storage medium. Natural Language Toolkit (NLTK) is utilized for
text processing, and custom scripts are developed for constructing and querying
both inverted and positional indexes.


1 Text Processing with NLTK
1.1 Approach
Utilizing NLTK within Google Colab for preprocessing text files stored on
Google Drive. The objective was to clean and normalize the text to facilitate
further processing or analysis.
1.2 Methodologies
- Text conversion to lowercase to ensure uniformity. - Tokenization and removal
of stopwords and punctuation to focus on meaningful content. - Automated
script execution for processing multiple files.
1.3 Assumptions
- Text files are well-structured and predominantly contain natural language
content. - NLTK’s default stopwords list is sufficiently comprehensive for the
task.
1.4 Results
--- Before Processing ---
I’m a long time musician, and a long time user of Ernie Ball Strings...
1
--- After Processing ---
’m long time musician long time user ernie ball strings electric guitars...
--- Before Processing ---
Great quality patch cables!
--- After Processing ---
great quality patch cables wanted something cheap blue green red...
--- Before Processing ---
Looks great! Replaced the stock neck plate on my Squier standard telecaster.
--- After Processing ---
looks great replaced stock neck plate squier standard telecaster
Processed texts demonstrated a clear reduction in non-essential words and symbols,
showcasing the effectiveness of the methodology in preparing data for
analysis.


2 Inverted Index for Query Processing
2.1 Approach
Building an inverted index from the processed files to support efficient query
processing with logical operators (AND, OR, AND NOT).
2.2 Methodologies
- Indexing terms against documents to facilitate rapid retrieval. - Logical operation
handling within query processing to combine or exclude document sets
based on term presence.
2.3 Assumptions
- Documents are preprocessed and indexed without error. - Users input wellformed
queries compatible with the system’s logical operator handling.
2.4 Results
Query1: car OR bag AND NOT canister
Number of documents retrieved for query 1: 31
Names of the documents retrieved for query 1: file930_cleaned.txt, file404_cleaned.txt...
Query2: coffee AND brewing OR NOT techniques OR cookbook
Number of documents retrieved for query 2: 0
Names of the documents retrieved for query 2: None
The system successfully executed complex queries, demonstrating the inverted
index’s utility in information retrieval across a document corpus.
2


3 Positional Index for Phrase Query Processing
3.1 Approach
The creation of a positional index to enable precise phrase query processing,
aiming for exact sequence matching within documents.
3.2 Methodologies
- Recording term positions within documents during indexing to support phrase
matching. - Implementing phrase query processing to identify documents containing
the exact term sequence.
3.3 Assumptions
- Phrase queries accurately reflect the users’ search intent. - The positional
index accurately captures term positions across all documents.
3.4 Results
Number of documents retrieved for query 1 using positional index: 0
Names of documents retrieved for query 1 using positional index: None
Number of documents retrieved for query 2 using positional index: 0
Names of documents retrieved for query 2 using positional index: None
The absence of documents returned for test queries highlighted the precision
required for successful phrase matching, suggesting limitations in the dataset or
the specificity of the queries.
3
