todo.txt-cli-addons
===================

My custom addons for https://github.com/ginatrapani/todo.txt-cli

## recur ##
Similar to https://github.com/paulroub/todo.txt-recurring-tasks, but allows for 
Weekly, Monthly, Bimonthly, Quarterly, and Yearly recurrences.

### Dependencies ###
Requires a ruby interpreter. I've only tested it on 1.9.3. Let me know if it works
on any other versions.

Also requires the [todo-txt gem](https://github.com/samwho/todo-txt-gem) by @samwho.

### Usage ###
Create a recur.txt file in your TODO_DIR and adds tasks in the following format.
Then call `todo.sh recur` in a cron job every morning.

### recur.txt format ###
*   Blank lines and comments (anything after a '#') are ignored
*   Task lines must match this format: `<freq>, <date> - <text>`
* Where `freq` is one of:
  * Weekly - date is day of week (default Sunday)
  * Monthly - date is day of month (default 1st)
  * Bimonthly - like Monthly, but skip every other month (Start with Jan, but can specify another start month)
  * Quarterly - like Bimonthly, but skip every two months
  * Yearly - date is month and day (default Jan 1)

### Example recur.txt file ###
    
    Monthly, 28th - (A) Give dog heartworm medicine @home
    Bimonthly, 1st - (B) Wash dog @home +chore
    Quarterly, 1st - (A) Reorder dog treats @home
    Yearly, July 1st - (A) Take dog to vet for shots, heartworm pills @car +errand
    
## standup ##
Similar to https://github.com/civrot/todo_txt_actions/blob/master/standup but
prints a weekly report (broken down by day) instead of a daily one.

## add ##
Just taken from https://github.com/ginatrapani/todo.txt-cli/wiki/Creating-Add-ons%3A-Examples,
but I think I fixed a bug. I don't remember what it was, though.

## nav ##
Taken from https://github.com/doegox/todo.txt-cli/blob/extras/todo.actions.d/nav,
with no modifications.

## lsn ##
Lists tasks with no priority.
