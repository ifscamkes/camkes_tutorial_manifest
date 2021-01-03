We are thankful to Data61 and seL4 developer's community for making CAmkES 3.5.0 available for free public use and development purposes.

Information Flow Secure CAmkES (IFS-CAmkES) is our initial attempt in making CAmkES based systems information flow secure. We have released IFS-CAmkES 1.0 in our endeavor to help the community and further colloboration to make it more robust.

We would be grateful for any suggestions towards improving IFS-CAmkES.

# Installation and Usage Instructions

Set up your machine to to build and run seL4 and CAmkES:
https://docs.sel4.systems/projects/buildsystem/host-dependencies.html

Browse and download the required git repository available at: https://github.com/ifscamkes
1. camkes_tutorial_manifest is the repository for information flow secure CAmkES
2. original_camkes is the repository for original CAmkES (camkes-3.5.0)

In the camkes_tutorial_manifest repository, all the Information Flow Secure CAmkES examples are available at: 
camkes_tutorials_manifest/projects/sel4-tutorials/tutorials

### To run a project:
1. Change the example name to hello-camkes-1
2. In camkes_tutorials_manifest directory, run the following commands:

   a. mkdir <project_name>
   
   b. cd <project_name>
<<<<<<< HEAD

=======
   
>>>>>>> 8099690a39c051a9d0436331c5daee930eba7f46
   c. ../init --plat pc99 --tut hello-camkes-1 [--rwfm_set] [--print_labels]
   
        I.  If you want to use rwfm then use --rwfm_set flag
      
        II. If you want to print the rwfm labels use --print_labels flag.
      
<<<<<<< HEAD
          Both these flags work only in information flow secure CAmkES.
=======
        Both these flags work only in information flow secure CAmkES. 
>>>>>>> 8099690a39c051a9d0436331c5daee930eba7f46
          
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
3. hello-camkes-1-bidding: Demonstrates that RWFM helps in safe bidding i.e. the bidders do not get to know each others bids and result apriori.
4. hello-camkes-1-paper-leak: Demonstrates RWFM helps in preventing the paper leak from TA to students.
5. hello-camkes-1-rpc-call: Demonstrates RPC Call from Client 1 to Echo to Client 2.
6. hello-camkes-1-rpc: Demonstrates RPC from Client 1 to Echo to Client 2. 
7. hello-camkes-1-multiple-rpc-calls: Demonstrates multiple RPC Calls from Client 1 to Echo to Client 2.
8. hello-camkes-1-multilple_rpc: Demonstrates multiple RPC from Client 1 to Echo to Client 2.
9. hello-camkes-1-timing-rpc: To calculate the number of RPC in 100 seconds with RWFM. (Use camkes_tutorials_manifest/timing.sh to run it, after changing the example name to hello-camkes-1)
10. hello-camkes-1-timing-rpc-call: To calculate the number of RPC Calls in 100 seconds with RWFM. (Use camkes_tutorials_manifest/timing.sh to run it after changing the example name to hello-camkes-1)