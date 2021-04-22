All IFS-CAmkES examples are available at: ifs-camkes/projects/sel4-tutorials/tutorials

## To run a project:
1. Change the example folder name to hello-camkes-1
2. In ifs-camkes directory, run the following commands:

   a. mkdir <project_name>
   
   b. cd <project_name>
   
   c. ../init --plat pc99 --tut hello-camkes-1 [--rwfm_set] [--print_labels]
   
        I.  If you want to use rwfm then use --rwfm_set flag
        
        II. If you want to print the rwfm labels use --print_labels flag.
        
        Both these flags work only in IFS-CAmkES. 
   
   d. ninja
   
   e. ./simulate

Ids for components and interfaces can be found in <project_name>/rwfm_log file as follows: 

## Format for component:
(component object -> (component name, id, component type))
## Example:
(<camkes.ast.objects.Component object at 0x7fe8c8bd2a50> -> ('client2', 2, <class 'camkes.ast.objects.Component'>))

## Format for interface:
(interface object -> (interface name, id, interface type, parent))
## Example:
(client1.h2 -> ('h2', 6, <class 'camkes.ast.objects.Uses'>, 'client1'))

Here is a brief overview of the examples: 
1. hello-camkes-1-indirect-write: Demonstrates that RWFM helps in stopping indirect write from Client 1 to Client 2 via Helper.
2. hello-camkes-1-indirect-read: Demonstrates that RWFM helps in stopping indirect read by Client 1 from Client 2 via Helper. 
3. hello-camkes-1-rpc-call: Demonstrates RPC Call from Client 1 to Echo to Client 2.
4. hello-camkes-1-rpc: Demonstrates RPC from Client 1 to Echo to Client 2. 
5. hello-camkes-1-multiple-rpc-calls: Demonstrates multiple RPC Calls from Client 1 to Echo to Client 2.
6. hello-camkes-1-multilple_rpc: Demonstrates multiple RPC from Client 1 to Echo to Client 2.
7. hello-camkes-1-timing-rpc-call: To calculate the number of RPC Calls in 100 seconds. (Use ifs-camkes/timing.sh to run it, after changing the example name to hello-camkes-1)
8. hello-camkes-1-timing-rpc: To calculate the number of RPC in 100 seconds. (Use ifs-camkes/timing.sh to run it, after changing the example name to hello-camkes-1)
9. hello-camkes-1-bidding: Demonstrates that RWFM helps in safe bidding i.e. the bidders do not get to know each others bids and result apriori.
10. hello-camkes-1-paper-leak: Demonstrates that RWFM helps in preventing the paper leak from TA to students.
11. hello-camkes-1-gps-tracking: Demonstrates that RWFM helps in preventing navigation server from leaking the location details to intruder.
