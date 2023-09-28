## Grep assignment
_Assignment_

- Cd to the directory /exercise-data/writing 
- Create a for loop that you will use on the LittleWomen.txt
- The loop should count the names "Jo" , "Meg", "Beth", "Amy"
- And prints the output on the screen

## Solution 
- for j in Meg Jo Beth Amy; 
- do 
- echo $j; less LittleWomen.txt | grep $j |wc -l; 
- done

## Output
Meg
685
Jo
1528
Beth
463
Amy
643


## Sed assignment

_Assignment_

- Use the sed command in a for loop to remove the following lines in the file diary.html
- 1 to 221
- 265 to 330
- Save the ouptput in a file called diary_no_header-no_footnote.txt

## Solution
- for a in '1,221d;265,330d'; 
- do 
- sed $a diary.html > diary_no_header-no_footer2.txt;
- done

