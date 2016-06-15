# google-cloud-playground
Playground for trying out the different GCP features. Mostly Golang.

# Goals:

Try out:
- Datastore
- App Engine
- Cloud Engine
- Pub Sub
- ? App Engine Flexible, currently in US-only beta :'( 
- ? App Engine Memcache
- ...

# AE: 
- Overview of healthy, running CE instances
- Direct client to the "correct" CE instance, based on chat room (or whatever, let's call it SyncGroup)
- Show all messages (or whatever) sent through the CE instances


# CE:

Communicate status back to AE

Datasore / or files (not in AE) or sql  

Communcation: Pub Sub, or Memcache, or Datastore? or REST calls

Auto Scaling, for the CE instances:
- Reacts to CPU usage or something more custom

Load Balancing, for the CE instances:
 - Not HTTP load balancer, tcp/udp (layer 3) l.b.
 - Done by our AE code or by a Gogle Load balancer?

