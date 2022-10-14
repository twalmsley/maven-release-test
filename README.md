# Shows how to use mvn release plugin

This tries to deploy to a local directory called `releases` but doesn't seem to do that. It says it has put the files in the `releases` folder but it is empty - are the files going anywhere??

Steps:

1. Make code changes and check everything in.
1. `mvn release:prepare`
1. `mvn release:perform`
1. If anything goes wrong:
    1. `mvn release:rollback` and maybe
    1. `mvn release:clean`
1. Delete the tag if necessary:
    1. `git tag -d 1.0.0`
    1. `git push origin :1.0.0`

