Created on: 16-03-2025 13:08
Status: #idea
Tags: #distributed_systems #clocks 
# No Global Clock
Distributed systems are comprised of nodes that are 
- autonomous.
- each node has its own notion of time.

### Pros
- This makes clock drift and clock skew no problems, so each node doesn't have to buy expensive crystals to by in sync with other components 
- decreases the need for periodic checks with a centralized server that has the true "global clock"
### Cons
- We don't know the real-time events occur in
- This creates the problem of knowing how to schedule two events.
- makes debugging harder, because we never know whether an event happened before another.






-----------------
# References