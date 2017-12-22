# newbOS
I'm not the average macOS user. Still new, still learning. Since macOS 
doesn't really ships with the latest and greatest cli stuff, why not 
curate myself this thing.

## Got Brew?
Familiar with aptitude but then again, on macOS it's kinda 
"unavailable". You can always brew it. 

```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Update Nano
Latest and greatest!

```
$ brew install nano
$ echo "include /usr/local/share/nano/*.nanorc" > ~/.nanorc
```
restart terminal and walla!

## Upgrading Things?
Why not?

### Update Homebrew
```
$ brew update
```
### See what's outdated?
```
$ brew outdated
```
### Upgrade everything
```
$ brew upgrade
```
### Upgrade specific formula
```
$ brew upgrade <formula>
```
