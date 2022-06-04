# My opinion:

The code is great, I could barely point at something/logic that is wrong. While it is a well written code, using the repository pattern
I feel has a way of over complicating codes that should be simple. Eloquent on its own is a repository, so,
coming up with another repository on top of Eloquent is like adding another layer of code/pattern on a predefined layer.

If this was not done using the repository pattern, it will be service and events driven. 

The logics and code formatting are easy and simple to read, I had little/no issues reading through the code line by line
except some functions that I suppose are in a model somewhere that I don't know what they do specifically.

## I made slight changes, which are:

In my own opinion whenever we are eager loading, for the sake of efficiency, we should always select the fields
we want e.g with('author:id,first_name,last_name'), this is faster and more efficient than getting all the
user data from the DB.

In the BookingController, some things are hard coded, I think it should be avoided since we can access it directly from the collection.
It is possible that there is typographical issue in the hard coded string which can break the application or create unnecessary bug(s).

While these operator will work well "!= and/or ==" I feel it is appropriate and safer to make it strict using "=== or !==".

Since we are getting/fetching user history, I feel it is efficient to use the Auth::user() facade, instead of searching using user_id.

## These are just my opinion, I am still a junior developer so I am looking at it from my own perspective. Thank you.