# java-code-count-the-occurrence-of-each-word
package q28434;

import java.io.*;

import java.util.*;

public class WordFrequencyAnalyzer {

public static void

main(String[] args){

K

K

K

Scanner sc = new

→→→→Scanner(System.in);

→String fileName = sc.nextLine();

File file = new File(fileName);

if(!file.exists()){

→System.out.println("File

does not exist");

K

K return;

K }

→TreeMap<String, Integer>map =

new TreeMap<>();

try{

Scanner reader = new

Scanner(file);

while(reader.hasNext()){

K

→String word =

reader.next().toLowerCase();

word = word.replaceAll("

[^a-zA-Z0-9]","");

K

K

K

if(!word.isEmpty()){

map.put(word, map.getOrDefault(word,0)+1)

;

K }

K }

K

reader.close();

for (String

word:map.keySet()){

System.out.println(word+":

"+map.get(word));

>}catch(FileNotFoundException e){

System.out.println("File

does not exist");

{KK

}

}

K →sc.close();