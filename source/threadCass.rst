threadCass.py
=============

************************************************************************************************************************
**Purpose:** Stream in tweets about presedential candidates, and store the tweets in the appropriate table in Cassandra.
************************************************************************************************************************

**Inputs:** Tweets about presedential candidates via the Tweepy API
*******************************************************************

**Outputs:** Tweet fields compacted into rows that are put into Cassandra
*************************************************************************

.. literalinclude:: threadCass.py
    :language: python

