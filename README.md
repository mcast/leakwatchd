# leakwatchd (Vapourware!)

An idea for a tool to detect monotonic increase in resource usage; a memory leak watching daemon; some kind of filter for existing metric gathering systems.

## The problem

Every now and then, some process runs amok.  Usually this is by steadily consuming memory until either the [OOMkiller](https://en.wikipedia.org/w/OOM_Killer) fixes the problem brutally, or performance decreases so far that processing basically stops.

## The solution

Obviously, to watch the processes to see what is getting out of control.  But to do it in a way that is flexible and doesn't involve re-inventing too many wheels.

1. A process to stream relevant resource information, in some simple format.  Like [Metrics 2.0](http://metrics20.org/).
2. A filter to detect steady & significant monotonic growth of the resource usage of a process, on any timescale, and maybe predict time-to-failure.
3. Hooks into alert generators.

# Implementation

I made a quick web search and didn't find one.  This vapourware spec exists so that anyone else looking for the same can either find it and run with it, or let me know what they found or wrote.
