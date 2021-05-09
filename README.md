# LFPC-lab4
This is laboratory Nr.4 to the "LFPC" subject at university. The code creates the simple precedence parsing algorithm.

#### To parse you should write your grammar in the grammar.txt file. There is already written an example. The grammar you write in the file must respect this form:
1. Write all terminal symbols, one per line
2. After you finish writing the terminal symbols write 'next'
3. Next write all nonterminal symbols, one per line
4. After you finish writing all nonterminal symbols write 'next'
5. Then write all the rules, one per line in the following form: "Symbol -> Symbols". Between arrow and symbols is one space. Empty productions are written with 'e', for example 'B -> e'.
6. The last line should be written 'next'
7. Write the string you want to be analyzed and Enter
8. Save the grammar.txt

#### Example:
###### a
###### b 
###### next
###### S
###### A
###### B
###### next
###### S -> aA
###### A -> bB
###### B -> ab
###### B -> e
###### next
###### abe

#### Every block in Main.ipynb represent a function. Every functions' name are maximum explcit, for example: read() -> reading the grammar from grammar.txt, elimintations_of_e_productions -> elimination of every empty production from context free grammar, etc
#### The main block is the last one. In the program are used global variables: terminal_symbols (for storing terminal symbols), nonterminal_symbols (for storiing all nonterminal symbols), rules (for storing the rules of grammar), rules_dic (the dicitionaries where are stored the rules in another form), first_last (the dictionary to store the relation for first-last table), to_analyze_string (the string which should be analyzed), matrix (2D list which stores the matrix of simple precedence) and all_symbols (the dictionary which stores all symbols and their nr.order in matrix). There are also another lists, but they are not global. After the variables declaration, there are all the functions for parsing with Simple Precedence algorithm.
#### After running every function there is printef the modiffied dictionary of rules to show what changes have beed made
#### intro(), read(), output_intro_data() - the grammar is read, then is printed the grammar you wrote in the grammar.txt to ensure it is correct.
#### grammar_to_dictionary() - is made the dictionary of rules out of rules list. It is used for further calculations in code. The dictionary is printed.
#### create_first_last_table() - this function created the the sets FIRST and LAST. Also it prints it. The data is stored in first-last dictionary
#### construct_matrix() - this function creates the matrix of simple precedence, using data made earlier in the code.
#### string_analyses() - this function analyze the string given as input. It prints all the steps made in the process of analysis.
