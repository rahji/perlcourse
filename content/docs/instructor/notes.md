---
title: My Original Notes
weight: 3
---

You may have a hard time understanding these original notes that I wrote when I was proposing a Perl course to the Cambridge Center for Adult Education. It basically lists what I hoped to include in an 8-week course (one day per week). I’m including it here for completeness, but you probably want to look at the outline and roadmap links.

## week 1

intro / free / interpreted / influences / perl6 / www / other uses / why environment / installation / requirements / isp command line / chmod / scripts / switches type and run a script perlstyle / documentation / common probs handout break numeric literals / math operators string literals / string operators x . .= / escapes / interpolation scalars / qq / here printf exercise with math and output

## week 2

more exercises / use string ops / printf / math \<STDIN\>,\<\> more later / chomp no chop exercise that takes input and outputs arrays / @ / 0-based list / creating / .. / qw list vs array undef and $x[0]=1 $x[2]=1 what’s $x[1]? / defined() more later handout quiz thing break interpolation & printing arrays list context vs scalar context $x=@x ($x)=@x size of arrays scalar() @ $# array slices $x[0] $x[$#x] $x[0..3] $x[1,4] split() and many other array functions / mention join() / handout for rest array exercises (read file and split)

## week 3

go over exercises more exercises / choose array functions from list – reverse sort rand other array functions break hashes / creating / fat comma / barewords keys / values / delete / exists vs defined / mention each hash exercises / show unique count example

## week 4

go over exercises control structures / code block expressions / true false 0 1 / eq vs == vs = logical operators / or vs || if-then-else elsif / unless / alt syntax exercises

## week 5

go over exercises remind about code blocks / labels while loop / with \<\> (next wk files) / remind chomp / each with hashes last / next / continue for / (;;) / similarity to other langs / mention nesting foreach / default var exercises

## week 6

files / \<\> vs \<STDIN\> / $. / @ARGV $ARGV $ARGV[0] $ARGV[1…] $#ARGV open() / read / append / truncating problem / close() die / STDOUT STDIN now STDERR while \<FILE\> / default var slurp @x=\<X\> eg FH in array context / @x = split(' ',\<FILE\>) eg filehandle in scalar context chomp($x = \<STDIN\>) / assign to hash chomp($x{asdf}=\<STDIN\>) mention read() and getc() exercises

## week 7

more exercises since we can do useful things now other sources of input / system() / backticks / qx break regexp / perlre / used as true false expression m / alt delimiters / s metacharacters / ^ $ . / quantifiers + * {} / char class [] / alternating (|) / grouping and backrefs negation (! m//) unless exercises

## week 8

go over exercises / more exercises reasons for using subs / syntax / return exercises discussion / web / dbms / cpan modules
