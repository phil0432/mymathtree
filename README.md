# mymathtree
Making a sequential script with different directories of addition, subtraction, multiplication and division. The script takes the arguments and stores the output in the required directory.

Code:

#!/bin/bash -u
PATH=/bin:/usr/bin ; export PATH
umask 022

rm -r -f mymathtree 2>/dev/null


mkdir -p mymathtree/add_and_sub
mkdir -p mymathtree/mul_and_div

# Store command line arguments as variables
num1=$1
num2=$2

# Perform calculations and write

expr $num1 - $num2 > mymathtree/add_and_sub/sub.txt
expr $num1 - $num2 > mymathtree/add_and_sub/sub.txt
expr $num1 \* $num2 > mymathtree/mul_and_div/mul.txt
expr $num1 / $num2 > mymathtree/mul_and_div/div.txt
