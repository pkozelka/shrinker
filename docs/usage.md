# Usage

Synopsis

    shrink <dirname>

Files

```
.shrink/
    CONTENT/             - the data that should be packed and sent over
        .unshrink/       - the files needed to restore all duplicate files
            version      - version of shrink used
            dups         - plaintext file, listing duplicates, one per line, in format "duplicatename=uniquename"
            unshrink.bat - windows batch restoring the duplicates
            unshrink.sh  - linux sh script restoring the duplicates, by reading `dups`
        *
    filesums
    dirsums
```


TODO:
- support files containing `=` by linking them into `.unshrink`
- check how support for other various chars works, like `/`, `~` etc.
