# ANSWER 26 9

**Question 9**

**What is the primary difference between Development Mode and Production Mode in DLT?**

**A. Development Mode supports only batch processing. ❌ Incorrect**

Development Mode supports both batch and streaming.

**B. Production Mode disables Unity Catalog integration. ❌ Incorrect**

Production Mode fully supports Unity Catalog.

**C. Development Mode keeps the cluster running for faster debugging, while Production Mode automatically terminates the cluster after execution. ✅ Correct**

Development Mode:

- cluster stays running

- rapid testing

- easier debugging

Production Mode:

- cluster starts automatically

- runs the pipeline

- shuts down afterward

- saves compute costs

**D. Production Mode cannot run Streaming Tables. ❌ Incorrect**

Production Mode fully supports Streaming Tables.

**E. Development Mode supports only SQL pipelines. ❌ Incorrect**

Development Mode supports:

- Python

- SQL

- streaming

- batch

**Why C is correct**

The key difference is **cluster lifecycle management**:

- Development Mode prioritizes developer productivity by keeping clusters available.

- Production Mode prioritizes cost efficiency by automatically terminating clusters after execution.

# [README](./../../../README.md)
