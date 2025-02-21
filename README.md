### Advanced Open Source Configuration

#### Playground Challenge - 4  
**Cassandra Kubernetes Deployment & Optimization (20 points)**

---

### Scenario
Your company is working on a cloud-native microservices application that needs a highly available, scalable, and optimized NoSQL database. The team has decided to use Apache Cassandra and deploy it on Kubernetes. As a database engineer, you have been assigned the task of:
1. Setting up the Cassandra cluster
2. Monitoring it
3. Running basic CQL commands
4. Optimizing its performance.


---

### Implementation Tasks (GitHub Codespaces)

- This GitHub repository will be accessible to you once you accept the Playground Challenge.
- You have to work directly in this GitHub repository. It is like your own copy of the original repository.
- Start a new Codespace. It will have Kubernetes preinstalled.

  Note that it may take around 5 minutes for the Codespace to start after you click on "Create Codespace".


#### **Part 1: Cassandra Setup on Kubernetes**

1. **Deploy a two-node Cassandra cluster on Kubernetes**:
   - Use the cassandra.yaml manifest file given to you
   - Replace the values of `<INPUT1>`, `<INPUT2>`, `<INPUT3>` before applying the manifest.

2. Verify the cluster is running and healthy
   - Check the status of the Kubernetes pods and filter the results using the approriate labels

---


#### **Part 2: Cassandra Cluster Monitoring**

1. Use nodetool to check the status of the cluster and ensure all nodes are in an UN (Up Normal) state.
2. Use nodetool info to gather resource usage metrics (disk space, memory, etc.).
3. Connect to one of the Cassandra nodes using cqlsh and ensure that you can execute CQL commands.

---

#### **Part 3: Running CQL Basic Commands**

1. Create a keyspace named **user_data** with replication factor 2.
2. Create a table **users** with columns id, name, and email.
3. Insert three records for the below users and query them to verify insertion:
   - Alice, alice@example.com
   - Terence, terence@example.com
   - Mike, mike@example.com
4. Login to the 2nd node and test if all the table data is accessible


---

#### **Part 4: Performance Optimization**

The development team complains that queries on the users table are slow. Complete the following tasks to resolve the issues.
1. Check the existing caching and the compaction strategies for the users table.
2. Implement a caching strategy to set the rows for each partition to 10.
3. Searching by email is frequently required. Optimize read performance of such queries by adding an appropriate indexing strategy.
4. Use batch write queries to insert 2 new user records into the table:
   - Priya, priya@example.com
   - Shahid, shahid@example.com
