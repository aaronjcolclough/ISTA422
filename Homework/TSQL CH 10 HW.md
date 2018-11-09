1. **What is the purpose of transactions? Why do we use transactions in SQL scripts?**

A transaction is a unit of work that might include multiple activities that query and modify data and that can also change the data definition.

2. **Briefly describe each of the ACID properties.**

Atomicity -  Either all changes in the transaction take place or none do.
Consistency - The term consistency refers to the state of the data that the relational database management system (RDBMS) gives you access to as concurrent transactions modify and query it.
Isolation - Isolation ensures that transactions access only consistent data.
Durability - After the commit instruction is recorded in the transaction log on disk, the transaction is considered durable even if the change hasn’t yet made it to the data portion on disk.

3. **What do we mean when we talk about the granularity of locks?**

how much of the data is locked at one time.

4. **What do we mean when we talk about the modes of locks?**

Lock modes specify different kinds of locks. The choice of which lock mode to apply depends on the resource that needs to be locked. The following three lock types are used for row- and page-level locking:
Shared (S)
Exclusive (X)
Update (U)

5. **In your own words, describe blocking, and give an example.**

blocking occurs when one connection (user process or application process) places a lock on a table (or a number of rows) and a second connection attempts to read or modify the data under the lock.

6. **What are the properties of locks? That is, list the column name and column type of the fields in sys.dm tran locks.**

resource_type   nvarchar(60)
resource_subtype  nvarchar(60)
resource_database_id  int
resource_description  nvarchar(256)
resource_associated_entity_id   bigint
resource_lock_partition   int
request_mode    nvarchar(60)
request_type    nvarchar(60)
request_status    nvarchar(60)
request_reference_count   smallint
request_lifetime    int
request_session_id    int
request_exec_context_id   int
request_request_id    int
request_owner_type    nvarchar(60)
request_owner_id    bigint
request_owner_guid    uniqueidentifier
request_owner_lockspace_id    nvarchar(32)
lock_owner_address    varbinary(8)
pdw_node_id   int

7. **What are the properties of sessions? That is, list the column name and column type of the fields in sys.dm exec connections.**

session_id    int
most_recent_session_id    int
connect_time    datetime
net_transport   nvarchar(40)
protocol_type   nvarchar(40)
protocol_version    int
endpoint_id   int
encrypt_option    nvarchar(40)
auth_scheme   nvarchar(40)
node_affinity   smallint
num_reads   int
num_writes    int
last_read   datetime
last_write    datetime
net_packet_size   int
client_net_address    varchar(48)
client_tcp_port   int
local_net_address   varchar(48)
local_tcp_port    int
connection_id   uniqueidentifier
parent_connection_id    uniqueidentifier
most_recent_sql_handle    varbinary(64)
pdw_node_id   int

8. **What are the requests of sessions? That is, list the column name and column type of the fields in sys.dm exec requests.**

session_id    smallint
request_id    int
start_time    datetime
status    nvarchar(30)
command   nvarchar(32)
sql_handle    varbinary(64)
statement_start_offset    int
statement_end_offset    int
plan_handle   varbinary(64)
database_id   smallint
user_id   int
connection_id   uniqueidentifier
blocking_session_id   smallint
wait_type   nvarchar(60)
wait_time   int
last_wait_type    nvarchar(60)
wait_resource   nvarchar(256)
open_transaction_count    int
open_resultset_count    int
transaction_id    bigint
context_info    varbinary(128)
percent_complete    real
estimated_completion_time   bigint
cpu_time    int
total_elapsed_time    int
scheduler_id    int
task_address    varbinary(8)
reads   bigint
writes    bigint
logical_reads   bigint
text_size   int
language    nvarchar(128)
date_format   nvarchar(3)
date_first    smallint
quoted_identifier   bit
arithabort    bit
ansi_null_dflt_on   bit
ansi_defaults   bit
ansi_warnings   bit
ansi_padding    bit
ansi_nulls    bit
concat_null_yields_null   bit
transaction_isolation_level   smallint
lock_timeout    int
deadlock_priority   int
row_count   bigint
prev_error    int
nest_level    int
granted_query_memory    int
executing_managed_code    bit
group_id    int
query_hash    binary(8)
query_plan_hash    binary(8)
statement_sql_handle    varbinary(64)
statement_context_id    bigint
dop   int
parallel_worker_count   int
external_script_request_id    uniqueidentifier
is_resumable    bit
page_resource   binary(8)

9. **What is an isolation level? Give an example of the operation of an isolation level.**

Isolation levels determine the level of consistency you get when you interact with data.

10. **(Not in the book.) What do we mean when we say that an object is serializable?**

Serialization is the conversion of an object to a series of bytes, so that the object can be easily saved to persistent storage or streamed across a communication link.

11. **What is an deadlock? Give an example of a deadlock?**

A deadlock is a situation in which two or more sessions block each other. 
