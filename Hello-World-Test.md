# Hello-World-Test

```bash

# 執行 Hello,World 指令，不要用最新版的 cromwell.jar 可能會有錯誤!!
# java -Dconfig.file=cromwell.conf -jar cromwell-36.1.jar run cromwell-sample/hello-world/hello.wdl -i cromwell-sample/hello-world/hello.inputs.json

[ec2-user@ip-10-0-141-58 ~]$ java -Dconfig.file=cromwell.conf -jar cromwell-36.1.jar run cromwell-sample/hello-world/hello.wdl -i cromwell-sample/hello-world/hello.inputs.json
[2019-04-29 02:35:03,75] [info] Running with database db.url = jdbc:hsqldb:mem:d7b588c8-99d9-4876-8013-5527d7f9c4b8;shutdown=false;hsqldb.tx=mvcc
[2019-04-29 02:35:11,64] [info] Running migration RenameWorkflowOptionsInMetadata with a read batch size of 100000 and a write batch size of 100000
[2019-04-29 02:35:11,65] [info] [RenameWorkflowOptionsInMetadata] 100%
[2019-04-29 02:35:11,73] [info] Running with database db.url = jdbc:hsqldb:mem:f45c90c8-d9d3-4e52-b728-65244c25b5db;shutdown=false;hsqldb.tx=mvcc
[2019-04-29 02:35:12,04] [warn] Unrecognized configuration key(s) for AwsBatch: auth, numCreateDefinitionAttempts, numSubmitAttempts
[2019-04-29 02:35:12,35] [info] Slf4jLogger started
[2019-04-29 02:35:12,64] [info] Workflow heartbeat configuration:
{
  "cromwellId" : "cromid-080fd63",
  "heartbeatInterval" : "2 minutes",
  "ttl" : "10 minutes",
  "writeBatchSize" : 10000,
  "writeThreshold" : 10000
}
[2019-04-29 02:35:12,74] [info] Metadata summary refreshing every 2 seconds.
[2019-04-29 02:35:12,81] [info] KvWriteActor configured to flush with batch size 200 and process rate 5 seconds.
[2019-04-29 02:35:12,81] [info] WriteMetadataActor configured to flush with batch size 200 and process rate 5 seconds.
[2019-04-29 02:35:12,86] [warn] 'docker.hash-lookup.gcr-api-queries-per-100-seconds' is being deprecated, use 'docker.hash-lookup.gcr.throttle' instead (see reference.conf)
[2019-04-29 02:35:12,90] [info] CallCacheWriteActor configured to flush with batch size 100 and process rate 3 seconds.
[2019-04-29 02:35:12,94] [info] JobExecutionTokenDispenser - Distribution rate: 1 per 2 seconds.
[2019-04-29 02:35:13,18] [info] SingleWorkflowRunnerActor: Version 36-858f647-SNAP
[2019-04-29 02:35:13,20] [info] SingleWorkflowRunnerActor: Submitting workflow
[2019-04-29 02:35:13,36] [info] Unspecified type (Unspecified version) workflow 7dad02fa-645c-402e-ba36-5a39ba21d769 submitted
[2019-04-29 02:35:13,41] [info] SingleWorkflowRunnerActor: Workflow submitted 7dad02fa-645c-402e-ba36-5a39ba21d769
[2019-04-29 02:35:13,43] [info] 1 new workflows fetched
[2019-04-29 02:35:13,43] [info] WorkflowManagerActor Starting workflow 7dad02fa-645c-402e-ba36-5a39ba21d769
[2019-04-29 02:35:13,44] [info] WorkflowManagerActor Successfully started WorkflowActor-7dad02fa-645c-402e-ba36-5a39ba21d769
[2019-04-29 02:35:13,44] [info] Retrieved 1 workflows from the WorkflowStoreActor
[2019-04-29 02:35:13,46] [warn] SingleWorkflowRunnerActor: received unexpected message: Done in state RunningSwraData
[2019-04-29 02:35:13,48] [info] WorkflowStoreHeartbeatWriteActor configured to flush with batch size 10000 and process rate 2 minutes.
[2019-04-29 02:35:15,43] [info] MaterializeWorkflowDescriptorActor [7dad02fa]: Parsing workflow as WDL draft-2
[2019-04-29 02:35:16,25] [info] MaterializeWorkflowDescriptorActor [7dad02fa]: Call-to-Backend assignments: wf_hello.hello -> AWSBATCH
[2019-04-29 02:35:17,96] [info] WorkflowExecutionActor-7dad02fa-645c-402e-ba36-5a39ba21d769 [7dad02fa]: Starting wf_hello.hello
[2019-04-29 02:35:18,97] [info] Assigned new job execution tokens to the following groups: 7dad02fa: 1


[2019-04-29 02:35:20,00] [info] AwsBatchAsyncBackendJobExecutionActor [7dad02fawf_hello.hello:NA:1]: echo "Hello World! Welcome to Cromwell . . . on AWS!"
[2019-04-29 02:35:20,29] [info] Submitting job to AWS Batch
[2019-04-29 02:35:20,30] [info] dockerImage: ubuntu:latest
[2019-04-29 02:35:20,30] [info] jobQueueArn: arn:aws:batch:us-west-2:326623638833:job-queue/default-68f510b0-6662-11e9-a5fe-0af0816e310e
[2019-04-29 02:35:20,30] [info] taskId: wf_hello.hello-None-1
[2019-04-29 02:35:20,30] [info] hostpath root: wf_hello/hello/7dad02fa-645c-402e-ba36-5a39ba21d769/None/1
[2019-04-29 02:35:22,86] [info] AwsBatchAsyncBackendJobExecutionActor [7dad02fawf_hello.hello:NA:1]: job id: 0ad4f8fe-3a54-4033-8b05-fe85fca3a1ed
[2019-04-29 02:35:22,93] [info] AwsBatchAsyncBackendJobExecutionActor [7dad02fawf_hello.hello:NA:1]: Status change from - to Initializing
[2019-04-29 02:37:27,57] [info] AwsBatchAsyncBackendJobExecutionActor [7dad02fawf_hello.hello:NA:1]: Status change from Initializing to Succeeded
[2019-04-29 02:37:29,51] [info] WorkflowExecutionActor-7dad02fa-645c-402e-ba36-5a39ba21d769 [7dad02fa]: Workflow wf_hello complete. Final Outputs:
{
  "wf_hello.hello.message": "Hello World! Welcome to Cromwell . . . on AWS!"
}
[2019-04-29 02:37:29,54] [info] WorkflowManagerActor WorkflowActor-7dad02fa-645c-402e-ba36-5a39ba21d769 is in a terminal state: WorkflowSucceededState
[2019-04-29 02:37:53,33] [info] SingleWorkflowRunnerActor workflow finished with status 'Succeeded'.
{
  "outputs": {
    "wf_hello.hello.message": "Hello World! Welcome to Cromwell . . . on AWS!"
  },
  "id": "7dad02fa-645c-402e-ba36-5a39ba21d769"
}
[2019-04-29 02:37:57,87] [info] Workflow polling stopped
[2019-04-29 02:37:57,88] [info] Shutting down WorkflowStoreActor - Timeout = 5 seconds
[2019-04-29 02:37:57,88] [info] Shutting down WorkflowLogCopyRouter - Timeout = 5 seconds
[2019-04-29 02:37:57,89] [info] Shutting down JobExecutionTokenDispenser - Timeout = 5 seconds
[2019-04-29 02:37:57,89] [info] JobExecutionTokenDispenser stopped
[2019-04-29 02:37:57,89] [info] Aborting all running workflows.
[2019-04-29 02:37:57,90] [info] WorkflowStoreActor stopped
[2019-04-29 02:37:57,91] [info] WorkflowLogCopyRouter stopped
[2019-04-29 02:37:57,91] [info] Shutting down WorkflowManagerActor - Timeout = 3600 seconds
[2019-04-29 02:37:57,91] [info] WorkflowManagerActor All workflows finished
[2019-04-29 02:37:57,91] [info] WorkflowManagerActor stopped
[2019-04-29 02:37:58,13] [info] Connection pools shut down
[2019-04-29 02:37:58,13] [info] Shutting down SubWorkflowStoreActor - Timeout = 1800 seconds
[2019-04-29 02:37:58,13] [info] Shutting down JobStoreActor - Timeout = 1800 seconds
[2019-04-29 02:37:58,14] [info] Shutting down CallCacheWriteActor - Timeout = 1800 seconds
[2019-04-29 02:37:58,14] [info] CallCacheWriteActor Shutting down: 0 queued messages to process
[2019-04-29 02:37:58,14] [info] Shutting down ServiceRegistryActor - Timeout = 1800 seconds
[2019-04-29 02:37:58,14] [info] Shutting down DockerHashActor - Timeout = 1800 seconds
[2019-04-29 02:37:58,14] [info] Shutting down IoProxy - Timeout = 1800 seconds
[2019-04-29 02:37:58,14] [info] SubWorkflowStoreActor stopped
[2019-04-29 02:37:58,14] [info] JobStoreActor stopped
[2019-04-29 02:37:58,14] [info] CallCacheWriteActor stopped
[2019-04-29 02:37:58,14] [info] KvWriteActor Shutting down: 0 queued messages to process
[2019-04-29 02:37:58,14] [info] WriteMetadataActor Shutting down: 0 queued messages to process
[2019-04-29 02:37:58,15] [info] IoProxy stopped
[2019-04-29 02:37:58,15] [info] DockerHashActor stopped
[2019-04-29 02:37:58,15] [info] ServiceRegistryActor stopped
[2019-04-29 02:37:58,16] [info] Shutting down connection pool: curAllocated=1 idleQueues.size=1 waitQueue.size=0 maxWaitQueueLimit=256 closed=false
[2019-04-29 02:37:58,16] [info] Shutting down connection pool: curAllocated=0 idleQueues.size=0 waitQueue.size=0 maxWaitQueueLimit=256 closed=false
[2019-04-29 02:37:58,16] [info] Shutting down connection pool: curAllocated=0 idleQueues.size=0 waitQueue.size=0 maxWaitQueueLimit=256 closed=false
[2019-04-29 02:37:58,18] [info] Database closed
[2019-04-29 02:37:58,18] [info] Stream materializer shut down
[2019-04-29 02:37:58,18] [info] WDL HTTP import resolver closed

```