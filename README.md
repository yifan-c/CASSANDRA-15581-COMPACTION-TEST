# CASSANDRA-15581-COMPACTION-TEST

Results from the CASSANDRA-15581 compaction testing.

## Test Environment

- 3 nodes cluster. 
- Same resources provisioned for each container. (1 node per contianer)
- 200+GB of data per node. 
- Single table. 
- Load driven by tlp-stress with the same custom workload.

## Test Plan

1. Run data prepopulation

2. Run steady state load for X seconds as Phase 1.

3. Make one test case dependent change, e.g. triggering garbagecollect, altering table, etc., and 
continue the steady state load for Y seconds as Phase 2.

4. Compare the performance metrics beween Phase 1 and Phase 2.
