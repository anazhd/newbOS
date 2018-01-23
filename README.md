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

## Disk Utility Is Stupid
Be less stupid with a quick fix for simple task. Don't be like apple making the weird mediakit thing broken, can't do anything with drive (except on rare occasion). Disk Utility works 1 out 100 times.

### List Disk
```
diskutil list
```

### Force Unmount
```
diskutil unmountDisk force diskX
```

### Zero the boot sector
```
sudo dd if=/dev/zero of=/dev/diskX bs=1024 count=1024
```

### Partition It
```
diskutil partitionDisk diskX GPT <TYPE> "My External HD" 0g
```
type can be JHFS+, APFS, and I don't know what else. I just use APFS
