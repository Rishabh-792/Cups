# Adding Printer
Added the printer using lpadmin command
```
lpadmin -p test -E -v file:/dev/null
```

To create a print job :
```
lp -d test <file_name>
```
