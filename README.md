# Intro to Polymer

The project is geared to teaching the basics of polymer.

Objective: Start with a non-working gif search feed and work on fixing the several issues so that typing in the search bar automatically searches giphy for gifs!

### Setup

##### Prerequisites

[Bower](http://bower.io)


### Start the development server

 `python -m SimpleHTTPServer`

 App is now visible at `http://localhost:8000`

### Working on solution

1. In gif-feed.html fix it so that the query variable is plugged into URL and funny gifs are shown.
2. Now, in main-app.html, import and add the search-field component.
3. Typing in search field does nothing... we need to do 2 things:
    - Let the parent know the query property changed by setting notify:true on the property named query.
    - Gif-feed needs to observe for changes using an observer.
4. At this point you are getting gifs to appear as you type. It's not efficient right now, since it searches on every keystroke. Use this.debounce to search only once user stops typing.
5. Success!