I took Ben's Script from https://github.com/BenScarb/DownloadMagPi and knocked up a quick Dockerfile so I could run it on my Synology NAS without worrying about messing up/creating conflicts for python and dependencies.

You can run it with the following docker one-liner (add in the path you want the files downloaded to where it says `/YOUR/PATH/HERE` )

```docker run -it --rm -v /YOUR/PATH/HERE:/downloaded --name magpi-hoard  matstace/downloadmagpi```

-------------------------

# DownloadMagPi
Python Script to download the main MagPi magazine (Windows, Linux and Mac)

Edit the all_issues.py file, change the "output_dir" to the place you want the files stored, then set it running.
There's an additional "DoBackIssues" flag, set it to True and as well as the latest issues, it'll check all the previous ones too.

all_issues.py uses a RegEx to search the page for the download links, depending on the URLs in the URL list, it'll get all the types of available PDFs from the Foundation.

Run it each month to get the latest issue.  Something for a Cron job :)

TODO:
 1. ~~Work out why the TODO list is all on one line! (something to do with
    line breaks..)~~ (Used a wysiwyg editor)
 2. Improve Error handling (as there is some now)
 3. Perhaps make it in to a class

