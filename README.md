# Image_Caption_Generation_Flickr8k

Summary of Annotation Work:

dataT.txt: dataset with 1000 images and their 5 sentences each.

resultId.txt: list of 1k Ids.

resultSen.txt: list of 1k X 5 sentences.

DataCleaning1k.py: extracts Ids and Sen from dataT to resultId and resultSen.

convertJson.py: Creates Json file from Flicker8k_Dataset.txt, resultId.txt and resultSen.txt

jsonOutput1.txt: Json format for 1k images and their sentences.

resultSenWithoutColors.txt: removed colours from resultSen.txt

jsonOutput2.txt: Json format for 1k images and their sentences without colours.

Flicker8k_Dataset: 8091 Images

Flicker8k_DatasetList.txt: List of all the image Ids from Flicker8k_Dataset.

Flickr8k.token.txt: List of 8092 X 5 Sentences and their Ids.

2258277193_586949ec62.jpg is not present in Flicker8k_Dataset, hence been removed from Flickr8k.token.txt manually. 
FindID.py used to find the missing Id.

DataCleaning8k.py: Converts file into Json using Flickr8k.token.txt and whichever file you want to convert to Json.

resultSen8k.txt: list of all the sentences extracted from Flickr8k.token.txt

resultSen8k1S.txt: list of all sentences with modification for Json ( \” instead of “).

Json8kOutput.txt: JSON file for 8091 images and its corresponding 5 sentences.

resultSen8kPos.txt: Manually corrected output of resultSen8k.txt after passing through Stanford Parser.

SequenceCheck.py: Script for correcting the total number of sentences. Error caused because

Stanford Parser states a new sentence after detecting an exclamation mark and full stop. Index of Sentences which had this issue: 318,2384,2407, 8492,9076,10650,10646, 14837,21217, 22709, 26141,26788,30317,36032, 38116, 38555.

resultSen8kWithoutColors.txt: 8k sentences with all the colours removed.

List of colours being removed: pink, red, orange, white, black, blue, green, yellow, grey, golden, brown, purple, maroon, silver.

resultSen8kWthoutAdjColors.txt: 8k sentences with all the colours which are Adjectives removed.

findAdj.py: Script to list down all the adjectives from resultSen8kPos.txt to adjectives8k.txt

ColorsAdjRemove8k.py: Script to remove all the colours which are also adjectives from resultSen8k.txt
