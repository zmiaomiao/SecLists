# RobotsDisallowed
The RobotsDisallowed project is a harvest of the Disallowed directories from the robots.txt files of the world's top websites--specifically the Alexa 100K.

This list of Disallowed directories is a great way to supplement content discovery during a web security assessment, since the website owner is basically saying "Don't go here; there's sensitive stuff in there!".

It's basically a list of potential high-value targets.

## The project

So what we did is take the Alexa Top 100,000 websites, download their robots.txt files, extracted all Disallowed directories, and then performed a bunch of cleanup on them (they are a mess) to make the lists as useful as possible during web assessments.

## How to use the project

You use the project by coming to the root and downloading the DisallowedDirectories files there. You can then plug them into your favorite web assessment tool/function, e.g., Burp Intruder.

The files are broken down into Top-n lists, which are sorted lists based on the most common directories found. But if you are pressed for time or are looking for the highest-value targets, check out the InterestingDirectories.txt file, which I blogged about here: https://danielmiessler.com/blog/the-most-interesting-disallowed-directories/.

If you want to see how the output is created, enter the 'Code' directory. There you can get the raw Alexa site list, the scripts that are used to download and manipulate the robots.txt files, etc.

## Credit

This concept is not new. The RAFT project was the first to do this, but the project is now dead and gone. And since the concept works best when it's kept up-to-date, we decided to give it a refresh in the form of RobotsDisallowed.

## Next steps

There are lots of things we want to do with this:

1. Write a cleanup script that prunes the least likely hits
2. Complete all one million sites
3. Create individual lists for the top 10, top 100, top 1000 directories, etc. So if you're pushed for time you can use one of the condensed versions.

More ideas welcome!

### Leaders

It's harder than it looks to make the list both comprehensive and usable. People tend to have some pretty silly stuff in their robots.txt files, and many of the entries are only useful for one site.

So we curate.

If you'd like to help out, feel free to submit issues to the repo or send pull requests.

Thanks!

### Credits

It's important to us to thank people when they help out with the project.

- Brad Wolfe for adding the epic Bash multithreading (yeah, you read that correctly; go check the code)
