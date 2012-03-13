---
layout: default
title: data sharing
category: projects
---
#Data Sharing
My team shares a lot of data with collaborators in a lot of places. The rules about where data is stored and how it is shared can be very restrictive, even if it is anonymized data. For this particular project, we had raw data for a few hundred subjects. Raw data couldn't be shared. Processed data *could* be shared, but it couldn't be easily aggregated: if you wanted the numbers for a certain subset of subjects, one of the researchers needed to babysit the finicky, long-running tool to build composite data. That's not very efficient. It's better if the researchers spend their time curing cancer and leave the data handling stuff to the data handling  people. 

There was one glimmer of hope: an old tool, written in pascal (!) that would aggregate finished data, at least in theory. However, it had some limitations: there was a hard-coded limit on data size that was too small, hard-coded pathnames for input and output files (so a website couldn't just shell out to it), etc. So I ported it to Java. I'm not a statistician--I just hang out with them in the cafeteria--so I didn't really understand the mathematical semantics of what the program was doing. But I went to college in the 80s, so I certainly knew pascal. My *wife,*, who is practically Amish, knows pascal. So I ported it like a monkey, re-implementing the algorithm loop by loop. By the end, the light turned on for me and I had a better idea of what was going on mathematically. I am still pretty sure that the original author ported his version from his slide rule algorithm.

My numbers matched the output of the original pascal to three or four decimal places...the precision of the floats were not the same, and there were a lot of products of a lot of logarithms. Fortunately, there were plenty of statisticians in the cafeteria, and they declared my results correct. They work with fuzziness all day and are comfortable with it.  Victory!  

For this application, it is natural for the users to tweak different parameters on the data until something jumps out at them, so it was natural to ship json-encoded data over the wire once and do all of the filtering and joining in the browser. If you ever have cause to do relational algebra on lists in javascript, let me recommend [Underscore.js](http://documentcloud.github.com/underscore/) for that kind of work. Having cross-platform _map_ and _filter_ and _intersect_ makes it very easy to bind list operations to the web controls, so that the user can add or remove filters as they like. 




