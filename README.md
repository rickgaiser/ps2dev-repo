## ps2dev-repo
A complete playstation 2 development environment using git and repo

### Get the sources
Create a directory for the development environment
```
mkdir ps2dev
cd ps2dev
```
Initialze the repo
This is only needed once
```
# Option1: init for git cloning the entire git repositories
repo init -u https://github.com/rickgaiser/ps2dev-repo -b master

# Option2: init for git cloning using --depth=1 (shalow clones, no history, faster)
repo init -u https://github.com/rickgaiser/ps2dev-repo -b master --depth=1
```
Get all sources (this will take some time)
Repeat this step every time you would to get the latest sources
```
# Option1: sync all
repo sync -j4

# Option2: sync only current branch, do not sync tags (faster)
repo sync -j4 -c --no-tags
```

### Build
The build-all script is a good first start.
- NOTE1: You need your environment variables setup correctly ($PS2DEV, $GSKITSRC, etc...)
- NOTE2: This will WIPE your $PS2DEV folder before rebuilding it.
```
./build-all.sh
```
