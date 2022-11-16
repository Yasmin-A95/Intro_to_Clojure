# Clojure

## Lore

Clojure was created by Rich Hickey in 2007

It's a member of the LISP family 

One of the powerful things about LISP family languages are LISP Macros which are easy to write, flexible, and less error prone. 

Clojure is a dynamically typed and functional language. 

Functional programming is a style of programming. Functional programming treats mutable state as a toxic absolute-last-resort-stinky measure. 

When a function does not use mutable state, it is referentially transparent - it always does the same work and returns the same value when envoked with the same set of arguments. 

These are pure functions. 

This process can be costly when the process of making coppies of large collections, however Clojure handles this functional programming problem in a unique way by having persistent collections

A persistent collection has immutable data, however it also had methods of efficiently making modified coppies. The new and old elements share memory slots for the elements which they have in common, and therefore needn't be recreated. 

What about I.O files? Resources like files, network resources,and user interactions are all inherently mutable. 

Statically typed functional languages use monad to sneak impure code into pure code.

Clojure however doesn't try to enfource functional purity, which makes the need for monad's a moot point (heheh). Any clojure function can be impure, you'd just be missing the point of clojure if you don't use it for functional programming. 

Functional programming seeks to be restrained with mutable state, Clojure leaves it to you to get that ratio right. 

To help you incorporate messy mutable state into your pure functional goodness, Clojure has reference types. So that the mutable code doesn't hurt your pure functional code as data is mutated across multiple threads of execution. If one function modifies it in a way other functions were not expecting, you've got problems.
A clojure reference holds mutable collection that stores just one element, and coordinates it across threads in order to syncronise code without using locks. 

Clojure runs on the JVM and relates strongly to Java. You can envoke Java within Clojure.

Clojure does include polymorphism, but abandons all other relationship to the Object Oriented world of Java.

### Repl 

"This is a string in Java and Clojure";
'this is not a string in either Java or Clojure';
'T'; this is a Java character;
53; a Java Long
6.2; a Java Double
nil; is a Clojure equivilent to the Java nul
foo; a Clojure symbol
:foo; a Clojure keyword (like a symbol but NOT one)
(1 2 3); a Clojure list, this is a singly linked list
[1 2 3]; a Clojure vector (you can use commas if you like), a tree of nodes which makes for random access of elements
{"foo" 3 4 5}; a Clojure map. an Unordered collection of key value pairs. Keys come before values. 