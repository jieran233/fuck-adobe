# fuck-adobe

A set of rules for Mihomo

I created a script that compares all Windows executable additions and deletions in `C:\` between two "snapshots". I used it to get a list of all executables added by installing PS

https://github.com/jieran233/execdiff

## Note

- The rules are created for PS only currently
- The rules assume PS is installed in the default location of `C:\`

## Usage

Add the content of `rules.yaml` to the top of routing rules in mihomo config
