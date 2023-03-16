---
title: Perl to PHP
bookFlatSection: true
weight: 3
---

I wrote this cross-reference a while back for people who know how to program using Perl and are looking for some familiar Perl functions in the php language. When I originally wrote it, we were stuck with php 3, so I later reworked the list to include some of the functions that were missing back then. (nb: that update was many years ago) There are obviously more differences between the two languages than the function-to-function cross-referencing that’s listed here but generally, it shouldn’t be a hard transition.

## Arrays

lists and hashes
: php doesn’t really discern between numerically indexed arrays (aka lists) and arrays indexed by key-strings (aka hashes aka associative arrays). Also remember that any kind of variable in php starts with a $, unlike perl which uses $ for scalars, @ for lists and % for hashes.

exists
: To check for the existence of a hash key in php, you should use array_key_exists().

map
: In perl, you can have some chunk of code execute on each element of a list. In php, you’ll use the array_walk() function which requires that you create a function that will be applied to each item in the list.

## Variables

delete
: In perl, it deletes a key and it’s associated value from a hash. In php, you probably want unset()

reset
: Woah there buddy, reset() does something different in php. In perl, it’s used to reset variables or ?PATTERN? searches – probably at the beginning of a loop. In php, it’s used to rewind an array back to the first element before you loop through it with a while loop or something.

undef
: In perl I’ve used it mainly for undefining a variable or a single element in a hash. In php, you’re probably looking for unset()

## Pattern Matching

s//
: To perform perl-style regular expression substitutions in php, use preg_replace(). Look at its ability to accept lists as arguments. Pretty handy.

m//
: To do perl-style regular expression matches in php, use preg_match()

tr//
: Use the strtr() function in php.

## Strings

chomp
: Use chop() or rtrim() (which are the same function) to remove whitespace and newlines at the end of a string. trim() and ltrim() come in handy too.

chop
: There isn’t a perl chop() in php. You’ll probably have to write your own function using substr().

lc, uc
: These functions are called strtolower() and strtoupper() in php.

lcfirst, ucfirst
: There’s no lcfirst() in php, but there is a ucfirst(). There’s also a ucwords().

quotemeta
: php has quotemeta(), but it’s also got addslashes(), htmlentities(), htmlspecialchars(). Check out the mysql_real_escape_string()

q, qq, qw, qx
: These quoting characters are really useful in perl, but don’t even think about it in php. This kind of loss of flexibility might seem frustrating at first, but in a weird way you get used to having less ways of doing the same thing. Less to remember? More uniform code? Don’t know.

ge, gt, le, lt, ne
: To compare strings in php, use strcmp(). The function returns zero if the two arguments match, so you should use it like so: if (strcmp($this,$that)==0) print "match"; Don’t make this mistake: if (strcmp($this,$that)) print "duh";

repeating a string
: In perl, you can print a bunch of dashes with something like print "-" x 20 but in php you have to use the str_repeat() function.

## Control Structures

backwards if statements
: You can’t do the cool perl backwards if statement (dosomething if condition) in php. You’ll have to be boring and do it with a normal if statement (if condition dosomething). There is, however, an alternate syntax for if statements that, like C, allows you to skip the curly braces.

do…until
: Basically the same, except it’s do...while in php. While and foreach loops are pretty much the same in both languages too.

elsif
: I get this wrong every time. It’s elseif (two e’s) in php. If you use an editor with syntax highlighting (like TextMate or vim) then it probably won’t be much of a problem for you.

goto
: Since php doesn’t use labels, it doesn’t have a goto. Probably not a bad thing.

last
: This is called break in php. If you want to jump out more than one level, pass a numeric value to continue. That tells it how many levels to jump out, unlike perl where you’d use labels to do this. Also, note that even though the php documentation says that php considers an if statement a loop as far as this stuff goes, it’s a lie.

next
: This is called continue in php. See the comments for last

sub
: Instead of defining subroutines, you define functions in php. The return() function is the same, though.

switch, case
: perl doesn’t have a switch. php does.

unless
: I like this feature of perl. php doesn’t have an unless. You’ll have to use an ugly if statement.

## Math

2^3 (exponentiation)
: In php, there’s no operator for this. Use the pow() function instead.

hex
: In php, it’s called hexdec(). Don’t forget printf() for formatting numbers. It’s identical in both languages.

rand, srand
: php has these, but apparently mt_rand() and mt_srand() are better. Another thing is that rand/mt_rand take two arguments – a minimum and a maximum – which makes life easier.

## Files

@array=\<FILEHANDLE\>
: To read an entire file into an array (each line in a separate array element) in php, use file()

eof
: Some of the file functions are the same as perl, except they have a letter ‘f’ in front of them. This is one of them: feof()

link
: To create a link in php, use symlink()

open, close
: Use fopen() and fclose() to open and close files in php. In php, you can open a url in the same way that you’d open a file. More function names that are the same as perl, but start with the letter ‘f’ — ftell(), fseek(), and fstat().

print FILEHANDLE
: Use fputs() or fwrite() (which are the same function) to print to a filehandle in php.

sysread
: Access the read system call with fread() in php.

## Miscellaneous

exec
: php has exec() and system(), but you should also take a look at passthru().

format
: I don’t think php has anything like the perl format stuff. Who cares?

localtime
: php has a localtime(), but it doesn’t allow you to use it as a scalar like you can in perl. If you’re messing with dates and times, though, you should start by looking at the date() function. It allows you do display and manipulate dates and times in a way that’s only possible with modules in perl.
