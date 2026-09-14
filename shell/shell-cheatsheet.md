
# Shell Scripting Cheat Sheet

Reference notes from my Shell Scripting learning journey (Days 16–21).

## Script Structure

#!/bin/bash
set -euo pipefail

- `#!/bin/bash` — Specifies Bash as the interpreter.
- `set -e` — Exit when a command fails.
- `set -u` — Treat unset variables as errors.
- `set -o pipefail` — Make pipelines fail if any command fails.

## Variables

name="Habeeb"
echo "$name"

## Command-Line Arguments

echo "$1"
echo "$2"

Useful special variables:

- `$0` — Script name
- `$1` — First argument
- `$#` — Number of arguments
- `$@` — All arguments

## Conditions

if [ "$value" -gt 10 ]; then
    echo "Greater than 10"
else
    echo "10 or less"
fi

## Loops

### For Loop

for item in apple banana orange; do
    echo "$item"
done

### While Loop

while [ "$count" -gt 0 ]; do
    echo "$count"
    ((count--))
done

## Functions

greet() {
    echo "Hello, $1"
}

greet "Habeeb"

## File Checks

- `[ -f "$file" ]` — Regular file
- `[ -d "$dir" ]` — Directory
- `[ -e "$path" ]` — Path exists

## Pipes and Redirection

command > output.txt
command >> output.txt
command < input.txt
command1 | command2

## Common Tools

grep
awk
sed
sort
uniq
head
tail
wc
cut

## Automation

Shell scripts can automate:

- System checks
- File management
- Backups
- Log analysis
- Package installation
- Maintenance tasks
