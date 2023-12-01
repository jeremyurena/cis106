---
name: Jeremy Urena
semester: Fall 23
course: CIS-106
---

#  Week Report 7: List of Commands and Their Uses

| Commands | What It Does                                                | Syntax                                    | Example                                                                                  |
| -------- | ----------------------------------------------------------- | ----------------------------------------- | ---------------------------------------------------------------------------------------- |
| cat      | display contents of a file                                  | cat + option + file(s) to display         | `cat todo.lst` and `cat ~/Documents/todo.lst`                                            |
| tac      | display the content of a file in reverse order              | tac + option + file(s) to display         | `tac todo.md` and `tac ~/Downloads/todo.md`                                              |
| head     | displays the top N number of lines of a file                | head + option + file(s)                   | `head ~/Documents/Book/dracula.txt` and `head -5 ~/Documents/Book/dracula.txt`           |
| tail     | displays the last N number of lines of a file               | tail + option + file(s)                   | `tail ~/Documents/Book/dracula.txt` and `tail 5 ~/Documents/Book/dracula.txt`            |
| cut      | extracts section of each line of file and displays          | cut + option + file(s)                    | `cut -d ':' -f1 /etc/passwd` and ` cut -d ':' -f1,7 /etc/passwd`                         |
| paste    | joins files horizontally in columns                         | paste + option + files                    | `paste users.lst ip_address.lst` and `paste -d ':' users1.lst ip_addresses.lst`          |
| sort     | sorts file                                                  | sort + option + file(s)                   | `sort users.lst` and `sort -r users.txt`                                                 |
| wc       | prints the number of lines, characters, and bytes in a file | wc + option + file(s)                     | `wc -m users.txt` and `wc -l users.txt`                                                  |
| tr       | translates or deletes characters from standard output       | Standard output l tr + option + set + set | `cat file.txt l tr '.' ','` and `cat file.py l tr -s "[:space:]" ' '`                    |
| diff     | compares files and displays the differences between them    | diff + option + file1 + file2             | `diff cars.csv cars-backup.csv` and `diff -y cars.csv cars-backup.csv`                   |
| grep     | search text in given file                                   | grep + option + search criteria + file(s) | `grep 'dracula' ~/Documents/dracula.txt` and `grep -i 'dracula' ~/Documents/dracula.txt` |

## The awk Command
awk is a scripting language used for processing and displaying text.

Formula:
- awk + options + {awk command} + file + file to save <--- (optional)

Examples:
- Print first field of /etc/passwd file
  - `awk -F: '{print $1} /etc passwd`
- Print last field of /etc/passwd file
  - `awk -F: '{print $NF} /etc passwd`
- Print first and last field of /etc/passwd file
  - `awk -F: '{print $1," = ",$NF} /etc passwd`
- Print first and 3 fields with line numbers
  - `awk -F: '{OFS="="}{print $1,$4}' /etc passwd`
- Start printing a file from a given line (exclude the first 2 lines)
  - `awk 'NR > 3 { print }' /etc passwd`

## The sed Command
SED is a stream editor that performs operations on files and standard output.

Formula:
- sed options + sed script + file

Examples:
- Replace a string in given file (replace pizza for rice)
  - `sed 's/pizza/rice' shopping-list.lst`
- Replace the number of occurrences of a pattern in a file
  - `sed 's/pizza/rice/4' shopping-list.lst`
- Replace all occurrences of a pattern in a file
  - `sed 's/pizza/rice/g' shopping-list.lst`
- Replacing string on a specific line number
  - `sed '3 s/pizza/rice' shopping-list.lst`
- Replace a string on a range of lines
  - `sed '1,3 s/pizza/rice' shopping-list.lst`