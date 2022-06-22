1.Create a folder named ‘sample’  in your ‘home’ directory
2.Inside ‘sample’ folder, create a file called ‘sample.txt’
Answer -  `mkdir sample && touch sample/sample.txt`

3.Add the following content to the file:
Hi! This is just a sample text file created using shell script.

Answer -
 `cat > sample/sample.txt << EOF
"Hi! This is just a sample text file created using shell script."
EOF`

4.Print the contents of the file.

Answer-
`while read -r CURRENT_LINE
    do
        echo "$CURRENT_LINE"
done < "sample.txt"`

5.Print the number of occurrences of letter ‘t’ in ‘sample.txt’
Answer-
`grep -o -i 't' sample.txt | wc -l`

6.Change the owner permissions to allow all the operations on the file. ( Read, Write, Execute )
answer-
`chmod u+rwx sample.txt`

7.Write command to append following content in sample.txt file:
Hi! This is just another sample text added to file.

answer-
`echo 'Hi! This is just another sample text added to file.' >> sample.txt`

8.Change the group permissions to allow only read operation.

Answer-
`chmod g-w sample.txt`
`chmod g+r sample.txt`

9.Change the all users permission to deny any sort of access to ‘sample.txt’
Answer-
`chmod u-rwx,g-rwx,o-rwx sample.txt`

10.Write command to create file named sample2.txt with content similar to that of sample.txt
Answer-
 `touch sample2.txt
 cp sample.txt sample2.txt`

11.Write command to print top 50 lines of file
answer-
`head -50 sample.txt`

12.Write command to print bottom 50 lines of the file
Answer-
`tail -50 sample.txt`

13.Add 5 files in the same folder named: prog1.txt, prog2.txt, program.txt, code.txt, info.txt
Answer-
`touch ./prog1.txt, prog2.txt, program.txt, code.txt, info.txt`

14.Write the command to list files which has “prog” in its name
answer-
`find . -name "prog" -print`
Getting issue for this one

15.What is the difference between source and sh commands?
Answer-
`Source - When it is called you load and execute a bash script into the current bash process.
Sh- when you call sh, you initiate a fork that runs a new session of /bin/sh.`

16.Write a command to get the difference between the contents in two files
`diff a.txt b.txt`

17.What is the difference between ls and lsof?
`ls - It lists all the folders of the current directory
Lsof - it shows the list of all open files in the system irrespective of the directory which we are currently in.`


18.Create directories ./hello/world (World dir is inside hello dir) using mkdir command where neither hello or world exists. It should be a single command without the use of &&.
`mkdir -p hello/world`

19.How can you permanently set an environment variables using a bash terminal?
Answer-
`nano /home/deq/.bashrc`

`export TEST="test variable"`

