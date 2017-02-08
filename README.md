# init as a new submodule 
ex. in the [root]/sensitive path of a different repo - in the root of the different repo, do:

        git submodule add git@github.jpl.nasa.gov:mbee-dev/ems-config.git sensitive

if git version < 1.7.5 (?)

        git submodule init
        git submodule update 

Commit and push .gitmodules and 'sensitive' path, the submodule should be on default (master) branch

# after init
- Cloning a repo that already have submodule, or switching to a branch that have submodule
if git version < 1.7.5 (?)

        git submodule update --init

the submodule may not be on a branch, to fix

        git submodule foreach git checkout master

# updating submodule to latest

        git submodule foreach git pull

this can update the submodule hash in the owning repo, if you commit the updated hash and other people get the update, they can do this to update their submodule 

        git submodule update --checkout

# Repository structure

1. alfresco
 * Alfresco (MMS) specific properties
2. mvn
 * Maven (Java project) specific properties
3. *.json
 * Angular specific properties
        
