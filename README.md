# Shows how to use mvn release plugin

Files are deployed to `./target/checkout/releases` as well as the local `~/.m2/repository`

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

Test Change
