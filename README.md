```
   /$$                                                                  /$$     
  | $$                                                                 | $$     
  | $$$$$$$   /$$$$$$  /$$   /$$ /$$  /$$  /$$  /$$$$$$   /$$$$$$  /$$$$$$$
  | $$__  $$ /$$__  $$|  $$ /$$/| $$ | $$ | $$ /$$__  $$ /$$__  $$/$$__  $$
  | $$  \ $$| $$$$$$$$ \  $$$$/ | $$ | $$ | $$| $$  \ $$| $$  \__/ $$  | $$
  | $$  | $$| $$_____/  >$$  $$ | $$ | $$ | $$| $$  | $$| $$     | $$  | $$
  | $$  | $$|  $$$$$$$ /$$/\  $$|  $$$$$/$$$$/|  $$$$$$/| $$     |  $$$$$$$
  |__/  |__/ \_______/|__/  \__/ \_____/\___/  \______/ |__/      \_______/
             create strings of hex compopsed of words
usage:
  PIPES: stdout source | ./hexword [filter] arg1 arg2 ... argn
  TEXT : ./hexword filename filter arg1 arg2 ... argn
    arg#=integer wordlength 	filename=wordlist* 
    filters: -lo		hex letters only, words with ABCDEF
*note:	     -ios		-lo plus I=1, O=0, S=5
 filter      -los		-lo plus L=1, O=0, S=5
 optional    -all<default>	-lo plus I,L=1**, O=0, S=5
	*: case insensitive, words delimited by spaces or newline 
	**: words with IL or LI in them are removed to avoid confusion
examples: 
   ./hexword dictionary.txt 8 4				->      B100D13DFACE
   echo "BEEF FOOD FIASCO DEEDED" | ./hexword -lo 4 6	->      BEEFDEEDED
   ```
