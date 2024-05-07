# Computer-Networking-Project---
* Communications and Information Engineering
* Team Project
* In this project, we will implement a transport protocol that provides some reliability services
on top of the unreliable UDP. This will be done by augmenting UDP with the GBN protocol.
An implementementation of a special GBN sender and receiver 

* Sender: 
The sender script should be called with three arguments: filename, receiver IP address,
receiver port. Other variables like the maximum segment size (MSS), window size N, and time-
out interval should be statically defined in the script.

* Receiver:
On running the receiver program, it deals with only one event: Reception of a packet. The
receiver parses the received packet separating the header and trailer information from the
application data and indicates via the user interface that a file is being received. If the packet
ID is the expected packet to be received, the application data is stored. Otherwise, the data is
discarded. Afterwards, the receiver sends an acknowledgment packet to the sender with the
ID of the last correctly received packet. When the last packet has been received, the receiver
then acknowledges the packet, writes the data to a new file, and indicates via the user
interface that the file reception is complete.


* Simulated loss:
As the network is small in our experiments, there is almost no packet loss. So, to test the
implemented protocol, packet loss will need to be simulated by randomly dropping some
packets at the receiver and assume that they were lost. Thus, for each received packet at the
receiver, generate a random number which decides whether the packet is lost or not. The
simulated loss rate should be in the range from 5% to 15%. Note that we will assume that
there are no errors introduced by the channel to the received packets, so there is no
checksum verification is needed.
