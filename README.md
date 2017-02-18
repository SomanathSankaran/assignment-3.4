# assignment-3.4
QN 1 IMPORTANCE OF NAMENODE IN HADOOP CLUSTER
NAMENODE is the master node It is responsible for proper functioning of cluster
1.It processes the client requests
2.It contains METADATA((ie) In simple terms if we consider these cluster as a book it is like the TABLE OF CONTENTS)
It does this by containing Fsimage and edit logs 
editLogs
It contains all transactions done on data
It keeps a copy of itself in the hard disk
FSImage
It contains the screenshop of all block at the start before any start of transaction.
and it sends a copy to secondary name node so that if primary name node fails this secondary name node could be  used.
(1.x version).But this updation of secondary name node  is on hourly  basis.So if primary name node fails there will be a loss.
To avoid this in hadoop 2.x version there is a process known as high availability where there are 2 name node namely active and  pasive name node(stand by) and the heart beat from data node are send to both these nodes as shown in fig(3.4.1)
so if active name node fails this passive name node can be used as an active and the old active node could be used 
4.Name node manages the meta data(creation,deletion of files,directories)
5.Name node also  maintains the blocks(heart beat management and block replication ,reporting etc)
