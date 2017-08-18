# Devel::NYTProf workshop

	https://metacpan.org/pod/Devel::NYTProf

## Existing Talks

Tim Bunce has given a few talks on Devel::NYTProf, most recently at the
Austrian Perl Workshop 2014:

	https://www.youtube.com/watch?v=SDWoCQf53Ck

Search youtube or slideshare for Devel::NYTProf and you will find the
rest. Tim talks more about the theory and implementation of profiling
that I am not going to cover here. This is more a demonstration of using
the module to profile *your* code and optimisation. So if you have some
code you want to profile then dig it out now

## Caveats

 * Don't do it!
 * Don't do it yet
 * Hardware is cheaper (and less error prone)
 * Don't guess
 * Make sure you have good test coverage
 * Do simple stuff first

## Setting Up

	cpanm Devel::NYTProf

## Using From The Command Line

	perl -MDevel::NYTProf ...

## Using Within A Script (start/stop/etc)

	use Devel::NYTProf;

 * Defer start
 * Early stop

## Viewing Profile

 * Flame graph
 * Top subroutine calls
 * All subroutine calls
 * Graphviz

## Digging Into The Details

 * Exploring code

## Looking For Optimisation Points

 * Frequently called subroutines / lines
 * Large Inclusive / Exclusive times
 * Deep subroutine stacks

 * DRY
 * Move accessors out of loops
 * Lazy logging: ->logger->debug( sub { ... } ); # when dumping structs

 * Things we can cache or memoize
 * Lazy loading in single run scripts
 * Blocking

## Framework plugins

	https://metacpan.org/pod/Mojolicious::Plugin::NYTProf
