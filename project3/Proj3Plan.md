- PING PONG periodic (10 second)
- recv PING
- recv PONG
  - update link costs
  - trigger **LS/DV update** when change
- port alive check (1 second) (threshold: 15 second)
  - a list to store alive ports (keep_alive_threshold)
  - trigger **LS/DV update** when change



- LS/DV periodic (30 second) 
  - initiate **LS/DV flood**
- recv LS/DV update
  - trigger **LS/DV update** when change
- LS/DV alive check (1 second) (threshold: 45 second)
  - a list to store alive LS/DV entries (keep_alive_threshold)
  - trigger **LS/DV update** when change



- **LS/DV update**
  - LS/DV algorithm
  - if entries updated, send the update out
  - update forwarding table ($arg_V(D(A,Y,V))$)



- **LS/DV flood**
  - send all the LS ($C(A,v)$)/DV ($D(A,Y)$) entries out



- recv Data packet (port number 0xFFFF)
  - forwarding table
- Test case