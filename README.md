kurippu(Note)
========

Kurippu - is a command line interface for Evernote,
It allows you to:
   * Create notes in your Evernote;  
   * Find notes in your Evernote;
   * Remove notes in your Evernote;
 

   
Kurippu has been written on Python, 

### The Problem Given By RajaRavivarma

1.Goto this website
    https://github.com/ginatrapani/todo.txt-cli
    
2.Develop a similar command line interface using Python/Ruby and Evernote API (http://dev.evernote.com/doc/)
    We prefer it in Python/Ruby but any language can be used

3.We expect these functionalities:

    1. Showing a list of created Notes.
    2. Saving a Note to Evernote along with a title.
    3. Deleting a Note, from the list.
    4. Adding tags to a Note (Optional)
    All of these pertain to Evernote API.

You may submit it on Tuesday. (24-Dec-2013) if you use Python/Ruby or a day before if you are using a well known language.


### Authorization in Evernote

    $ python kurippu.py login

This will start the authorization process. (Enter your Evernote Credentials)

### Logout 

    $ python kurippu.py logout


## Creating notes
### Synopsis
    $ python kurippu.py create --title <title>
                      --content <content>
                      [--tags <list of tags>]  
### Examples
    $ python kurippu.py create --title "IIT M Research Park"
                      --content "Modeled along the lines of successful research parks"
                      --tags "Research, innovation, TCS"


## Search notes in Evernote
### Synopsis
    $ python kurippu.py find --search <text to find>
                    [--tags <list of tags that notes should have>]
                    [--notebooks <list on notebooks where to make search >]
                    [--date <data ro data range>]
                    [--count <how many results to show>]
                    [--exact-entry]
                    [--content-search]
                    [--url-only]


    $ python kurippu.py find --search "IIT M Research Park"

	  Total found: 2
	    1 : IIT M Research Park 22.12.2013
	    2 : IIT M Research Park 24.12.2013
    
    $ python kurippu.py show 2
That will show you the note "IIT M Research Park 24.12.2013".


## Removing notes

### Synopsis
    $ python kurippu.py remove --notebook <note name>
                     [--force]

### Examples
    $ python kurippu.py remove --note "IIT M Research Park"

