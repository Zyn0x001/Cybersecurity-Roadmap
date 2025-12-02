**echo** - will output any text that we will Provide

**whoami** - it will print who am i (user name)

## File System (**ls , cd , pwd , mkdir, rm, rmdir, cp, mv , tree)

#### **ls**  - Listing (list all folder and file on current Dir/Folder)

ls [OPTION]... [FILE]...

- OPTION: modifies the behavior of the command.
- FILE: specifies which files or directories to list. If none is provided, it defaults to the current directory (.).


  **Commonly Used Options**
  **Option**	 **Description**
**-a**	Show all files, including hidden files (. and ..)
**-l**	Use long listing format (shows permissions, owner, size, etc.)
**-h**	With -l, print human-readable file sizes (e.g., 5K, 1M)
**-R**	List directories recursively
**-t**	Sort by modification time, newest first
**-S**	Sort by file size, largest first
**-r**	Reverse the order of the sort
**--color**	Enable colored output (usually default on modern systems)

**Example** - ls -alh

#### **cd** - Change Directory (Folder)

**Example** - cd /example

#### **pwd** - Print Working Directorys

**Example** - pwd

#### **mkdir** - Make Directory/ Creating Folder

**Example** - mkdir example [it will create a directory with the name of example]

**Example**
- mkdir newdir or folder name
- mkdir -p (create parents folders if needed)
- mkdir -p example/example/example
- mkdir -p lab/{room1,room2}/{notes,tools}
it will create folder  like this - 
lab/
├── room1/
│   ├── notes/
│   └── tools/
└── room2/
    ├── notes/
    └── tools/

#### **rm** - Remove [Removing file]

**Example** - re example.txt

#### **rmdir** - Remove Directories

**Example** - rmdir exmaple [it will delete exmaple named dir]

#### **cp** - copy

**Example** - cp exmaple.txt Desktop/etc

#### **mv** - move 

**Example** - mv example.txt home/Downloads


#### **tree** - → Shows directory structure as a tree

**Example** - tree 


**Example**

- rmdir [foldername]


### File Operations (cat, touch, cp, mv, rm)

#### **cat** - Concatenate (view inside of a file)

**Example** 
- cat 
- cat example.txt/pdf

#### **touch** - Create an empty file if it doesn’t exist or creating multiple file

**Example** 
- touch example.txt 
- touch example.txt test.txt file.txt
- touch [option]  example.txt


**option**
- 

#### **cp** - copy a file or directory
#### **mv** - move 
#### **rm** - remove
#### **del** - delete

## Search & Filters [find, grep, wc]

#### **find** - Finding for files or directory

- find [PATH] [OPTIONS] [EXPRESSION]

- PATH: Where to start the search (e.g., /, .).
- OPTIONS / EXPRESSION: What to search for and what to do with the results.

🔍 Commonly Used Options
Option	Description
**-name**	Search by file name (case-sensitive)
**-iname**	Search by file name (case-insensitive)
-type	Filter by file type (e.g., f, d, l, etc.)
-size	Filter by file size
-mtime	Modified time (in days)
-atime	Last accessed time
-ctime	Last status change time
-user	Belongs to specific user
-group	Belongs to specific group
-perm	File permissions
-exec	Execute command on result
-delete	Delete matching files (use with care!)
-empty	Find empty files or directories

**Example** - find /path/to/search -name "filename.txt"
- find -name example.txt
- find -rname example.txt
- find -name *.txt
- find Desktop/etc/ -type f -name "*.txt"
- find Desktop/ -type f -iname "*.txt"

**wc** 
- wc is used for Counting Line or text in a file.
**Example**
- wc -l example.txt [Counting Line]

**grep**

**Example** 
- grep "example/word/nUmber" example.txt
- grep "exmaple word" example.txt
- 


**Shell Operators**

**Symbol / Operator**	**Description**
- &	This operator allows you to run commands in the background of your terminal.
- &&	This operator allows you to combine multiple commands together in one line of your terminal.
- >	This operator is a redirector - meaning that we can take the output from a command or override a file (such as using cat to output a file) and direct it elsewhere.
- >>	This operator does the same function of the > operator but appends the output rather than replacing (meaning nothing is overwritten).


**Example** 
- cp example.txt /home/kali/Desktop/ &
- command1 && command2
- cat hey > example.txt    
- cat hello >> example.txt
- echo "user: admin pass: 12345" > example.txt
- echo "user: guest pass: guest" >> example.txt








