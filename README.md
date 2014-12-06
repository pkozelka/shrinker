# Shrinker

(Currently in development)


A tool that shrinks a directory before it is packed, making it easy to restore (unshrink) the content back to original.

## Goals

* the **unshrink** is a trivial operation, very easy to implement in any language
* initial implementation will be in bash (for the proof of concept)
* the implementation must be clean and straightforward enough to be easy to translate into other languages (C, Java, ...)
* when there is nothing to shrink, the directory must be left intact

## How it works

- computes checksum of each file
- computes checksum of each directory, using same technique as `git uses for dirs
- finds and removes duplicates based on checksums
- generates shrink info in a platform-agnostic way
- generates scripts for most platforms

Note: all generated files are stored in `.shrinked` directory

## Expected usage areas

Wherever files are highly duplicated:

- NodeJS packages, which have highly inefficient local storage
- image galleries
