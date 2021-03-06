---
layout: post
published: true
category: updates
title: Experimenting with Timelines
author: Peter Downs
---
For this project, I wanted to try out the the Knight Lab's [TimelineJS](https://timeline.knightlab.com/) tool for building interactive timelines. I'm normally more attracted to programming-heavy tools, but the point of htis class is partly to explore building tools for non-programmers: perfect.

Well, until I realized that the format the data came in didn't match the format that TimelineJS requires. Immediately I dropped into [IPython](http://ipython.org/). Using [Pandas](http://pandas.pydata.org/), I read in the original data (in a .xlsx file that I cannot otherwise open locally because my linux computer does not run Excel,) and wrote a short script to convert it into the appropriate format. The tricky part was really the date formats, everything else was a 1-1 mapping. For instance, I had to change a "Title" column to a "Headline" column -- simple.

Then, I output the data into a properly formatted `.csv` file and uploaded it to the Google Sheets spreadsheet that TimelineJS uses.

And that's it. Done! Very few other options are given. Prose won't allow me to embed an iframe, so you can [view the final result here](http://peterdowns.com/projects/timeline-example.html).

The biggest shortcoming I encountered is the lack of control over the display. If you look at the result, the events are crammed together and nearly unreadable. No events are given more visual weight than any other, so it's hard as an observer to understand what's worth reading and what isn't.

Moreover, this is a complicated timeline involving many different entities. It would be nice to be able to filter hte timeline by events involving specific characters in the action (George Bush, Ahmedinejad, etc.), as well as specific places or types of event (meeting, declaration, etc.)

It would also be useful to be able to group events into specific sub-narratives, and have the main timeline show these narratives at first instead of every little sub-event. Then, as the user explores deeper, can dig in and expand these narratives to get at the particular events.

Most importantly, I think the timeline should work vertically, rather than horizontally. The web is designed for documents that scroll vertically, and then the browser itself can be used to scroll around. Plus, this would easier allow for parallel timelines to be displayed.

Thinking back to Drucker's work, it might be nice to have multiple timelines overlayed; different commentary for the same events, from different perspectives. It would emphasize the humanity behind these events, and the fact that the descriptions are not just "facts" but interpretations thereof.