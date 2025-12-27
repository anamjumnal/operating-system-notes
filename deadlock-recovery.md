First let's know 
🔵What is a DEADLOCK?
➡️A process requests resources,if the resources are not available at that time,the process enters a waiting state.Sometimes a waiting process is never again able to change state,because the resources it has requested are held by other waiting processes.This situation is called DEADLOCK.

Now let's talk about
🔵DEADLOCK RECOVERY:
The system recovers from deadlock automatically.There are two options for breaking a deadlock 
🔴One is to simply abort one or more processes to break the circular wait
🔴The other one is to preempt some resources from one or more deadlocked processes.

1.PROCESS TERMINATION:-
  To eliminate deadlocks by aborting a process,use on of two methods.In both methods,the system  recovers/reclaims all the resources allocated to the terminated process.

💠ABORT ALL DEADLOCKED PROCESSES:-
  ⏺️This method will clearly break the deadlock cycle but at a great expense .
 🔶Let me tell you why
  ⏺️The process stuck in deadlock might have already run for a long time and done a lot of work.
  ⏺️When such a process is terminated to recover from deadlock,all the work it has done so far will be lost.
 ⏺️When the process is restarted later,it must repeat the same work again from beginning,wasting time and CPU resources.

  💠ABORT ONE PROCESS AT A TIME UNTIL THE DEADLOCK CYCLE IS ELIMINATED:-
 ⏺️This recovery method uses EXTRA CPU TIME,MEMORY USAGE,PROCESSING EFFORT AND SYSTEM RESOURCES,so this process is said to be OVERHEAD.
 ⏺️When one deadlock process is terminated,the system has to run the deadlock detection algorithm again.
 ⏺️The operating system checks if the deadlock has been completely removed or if other processes are still in deadlock.
 ⏺️This process is also known as PARTIAL TERMINATION METHOD.
  🔶To use this method,we must determine which deadlocked processes should be terminated.There are some factors to be considered-
  
  1.What the priority of the process is.
  2.How long the process has computed and hoe much longer the process will compute before completing its designated task.
  3.How many  and what types of resources the process has used.
  4.How many more resources the process needs in order to complete.
  5.How many processes will need to be terminated?
  6.Whether the process is interactive or batch.

  2.RESOURCE PREEMPTION:-
  ⏺️Preemption is an act of temporarily taking a resource from a process to resolve deadlock or to improve system performance.
 ⏺️To eliminate deadlocks using resource preemption,we successively  preempt some resources from processes and give these resources to other processes until the deadlock cycle is broken.
 ⏺️If preemption is required to deal with deadlocks,then three issues need to be addressed:

  🔶SELECTING A VICTIM-
    ⏺️Which resources and which processes are to be preempted?
    ⏺️A process termination,we must determine the order of preemption to minimize cost.
    ⏺️Cost factors may include such parameters as
    i)the number of resources a deadlocked process is holding
    ii)the amount of time the process has thus far consumed during its execution

  🔶ROLLBACK-
   ⏺️If we preempt a resource from a process,what should be done with the process?
    ⏺️Clearly,it cannot continue with its normal execution;it is missing some needed resource.
   ⏺️We must roll back the process to some safe state and restart it from that state.
    ⏺️Since it is difficult to determine what a safe state is,the simplest solution is to rollback:ABORT THE PROCESS AND RESTART IT.

  🔶STARVATION-
    ⏺️How do we ensure that the starvation will not occur?
    ⏺️How can we gurantee that resources will not always be preempted from the same process?

  
  

