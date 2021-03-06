.. _additional-configuration:

Additional Configuration and Limitations
----------------------------------------

1. Configuring the query timeout

   You can set the environment variable ``CLOUDLAUNCH_QUERY_CACHE_PERIOD`` before
   starting Galaxy to control the caching period. Setting this to 0 will allow you
   to get around the node removal issue (If a Pulsar node is removed, your jobs
   may be routed to a dead node for the duration of the caching period.), but we
   recommend setting a value to avoid repeatedly querying a remote server during
   each job submission.

2. Auto-scaling

   Currently, the GalaxyCloudRunner does not support automatic scaling, you must
   manually add and remove nodes. We will be adding autoscaling features as
   part of CloudMan v2.0 in future.

3. Galaxy versions prior to 19.01

   Galaxy versions prior to 19.01 do not support certain features required by
   GalaxyCloudRunner and therefore, need more complex configuration steps.
