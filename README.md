# problem_statement_4

<b>In this programme, we solve the following problem:</b><br>
Select random 10000 files from the train folder. For every file calculate the below values:<br>
File Name: basically the name of the file<br>
<li>Number of words in the file<br>
<li>Number of unique words in the file<br>
<li>Number of words that are in CAPITAL LETTERS ( example: This is a SAMPLE statement . this statement has one word “SAMPLE” that is fully capitalized )<br>
<li>Number of camelcase words<br>
<li>Number of lowercase numbers<br>
<li>Number of characters<br>
<li>Number of numeric characters<br>
<li>Number of non alphanumeric characters<br>
Once these values are calculated, write them to “Train_statistics.csv”. Format of the excel file should be as follows:<br>
File_name, num_words, num_unique_words, num_cap_words, num_camel_case_words, num_lower_case_letters, num_characters, num_num_characters, num_non_alpha_numeric_chars<br>

<b> Solution:</b><br>
First we create a function names <i>random_files():</i> which will select 10,000 random files from the <i>train</i> folder. Then we create 7 other functions which will help us perform operations required to extract information needed for the csv files. The functions are:
  <li><b><i>num_of_words_and_unique_words(fname)</i></b>
  <li><b><i>count_uppercase_letters(fname)</i></b>
  <li><b><i>count_lowercase_letters(fname)</i></b>
  <li><b><i>count_camelcase_words(fname)</i></b>
  <li><b><i>count_character(fname)</i></b>
  <li><b><i>count_numeric_character(fname)</i></b>
  <li><b><i>count_nonalphanumeric_character(fname)</i></b>
<br>
Finally a function named <b>process_files()</b> is created which helps to process each and every file individually in a loop, and their data is stored in a dictionary <i>dict{}</i>. This dictionary is then converted to a <b>DataFrame</b> using <b>Pandas</b> module, and then this DataFrame is writted into <b>output.csv</b> file
