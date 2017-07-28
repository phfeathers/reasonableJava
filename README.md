# reasonableJava
standardized approach to reduce work required to debug java servlet type project 

As the size of a servlet application grows, lack of a standard, thought out basis can lead to a lot of extra work, and testing can craw at a snail's pace.
For example: debugging the servlet application without proper planning can lead to requiring 2-4 concurrent monitors to display all the necessary debug information.
The first approach to solve this will be like this:
1) update templates in Netbeans to include your custom code for each type of template, in this case, starting with servlets, so
each new servlet will have included:
  a) company / institution info
  b) a custom class designed to display a standard set of debugging information at bottom of each displayed servlet --when running    in debug mode.
2) create a spec for how your program will know whether or not to display the debug data.
  a) environment variable
  b) system variable
  c) other  -- see Anderson's stackoverflow comments about when a JVM is in debug mode, etc.
3) is it possible / necessary to turn off this debugging code when compiling to production release?
4) update the logger to provide static logger proc for every class
5) standardize how your logger is used, and save into class template.
6) consider creating a custom form which selects which servlets, in debug mode, are not needing debug information.  So you have a 
way to go through, making the progress visually, until all you servlets are clean, not displaying debug info. -- a personal visual indicating one's progress.
