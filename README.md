# Stemming-From-Scratch
Stemming is the process of reducing inflected words to their word stem, base or root form—generally a written word form.

In this project, we have implemented stemming from scratch. We also display a graph between the count of unique words in the library and the number of words the compiler reads.

Each step has been neatly compiled into a function which is then called onto the main function. The steps followed are:

1. Read a .txt file and convert the data into lowercase
2. Remove acronyms from the text 
<p align="center">
  <b> Eg: U.S.A. → USA </b>
</p>

3. Tokenizing words(if separated by [‘ ‘, ‘,’, ‘;’.... anything except “ ‘ ” for single quotes(')]) 
<p align="center">
  <b> Eg: don’t should become dont </b>
</p>

4. Remove stop words from the given list <br>
5. Stemming:
  * If a word ends with “sses” and is not a small word, then convert to “ss”. 

<p align="center">
  <b> Eg:  stresses —> stress </b>
</p>

* If a word ends with “s” and the second last word is not a vowel but the remaining word contains a vowel, then delete the “s”. 
<p align="center">
  <b> Eg: gaps —> gap but gas —> gas </b>
</p>

* If a word ends with “ied” or “ies” and it is a small word, then delete the “d” or “s” respectively. 
<p align="center">
  <b> Eg: ties —»tie. </b>
</p>

* If a word ends with “ied” or “ies” and it is not a small word, then delete the “ed” or “es” respectively. 
<p align="center">
  <b> Eg: cries —» cri. </b>
</p>

* If a word ends in “eed” or “eedly” and contains a vowel followed by non-vowels which is then ended with the “eed” or “eedly” then, convert “eed” → “ee” or “eedly” → “ee”. 

<p align="center">
  <b> Eg: agreed —> agree, feed —> feed </b>
</p> 

* If a word ends with "edly", "ed", "ingly", "ing" and the remaining word contains a vowel:
  * And the remaining words end with either “at”, “bl”, “iz” or is a small word, then just add an “e”.
  * And the remaining word contains repeating last two letters except (“ll”, “ss”, “zz”) then remove the last letter.
6. Count the vocabulary increase as more words are read.
