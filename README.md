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

# Google Cloud Platform gotchas:

AE Classic:

- No filesystem
- No long runing requests
    - USed to be 30 seconds, 60 now
- GET or POST to other, how long timeout?
- No https for custom domains. (2010)
    - Fixed: https://cloud.google.com/appengine/docs/go/console/using-custom-domains-and-ssl#app_engine_support_for_ssl_certificates
- ikke alle libraries virker
 - bare pure python
 - ikke calle go libs (context etc), men de fleste (?)
- Slow for CPU intensive tasks (reportedly, makes sense)
- Priceing

 Datastore:
 - ? can't return > 1000 records?  (2010)
 - ? extremly slow writes (2013)
 - ? Datastore and memcache can fail sometimes (2010)

www.war-worlds.com/blog/2013/06/switched-away-from-app-engine-couldnt-be-happier (2013)
