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
