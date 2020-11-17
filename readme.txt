----------------------------------------------------------------------------------
IHUP-ID 
----------------------------------------------------------------------------------
	Incremental utility mining over data streams for a general model without restriction on insertion and deletion of transactions 

	Junqiang Liu ( jjliu @ alumni.sfu.ca ), et al.
----------------------------------------------------------------------------------
Citation Policy:
----------------------------------------------------------------------------------
If you publish material based on our algorithm, then, in your references, please cite one of the following:

[1] Junqiang Liu, et al. Incremental utility mining over data streams for a general model without restriction on insertion and deletion of transactions. Submission to Future Generation Computer Systems, November 2020. 

----------------------------------------------------------------------------------
Help 
----------------------------------------------------------------------------------
1. The implementation of our IHUP-ID algorithm in Java is:
	IHUP-ID.jar

2. Ten datasets are used in the experiments, one of which the mushroom dataset, which comes in two files:
	mushroom.txt      - the transaction file
	mushroomPrice.txt - the utility file 
   Moreover, the other 9 datasets will be uploaded soon. 

3. Each dataset is used to simulate a data stream by partitioning the dataset into batches using:
	myFileHandle        - a Linux executable for partitioning a transaction file into batches 
	myFileHandle64.exe  - a 64-bit Windows executable

4. The scripts for running an experiment on the mushroom dataset are as follows, which   
	test-mushroom-all-in-one.sh  - a Linux script
	test-mushroom-all-in-one.bat - a Windows batch file

5. The format of each dataset is in accordance with that in the experiments in the following paper. 
Y. Liu, W. Liao, and A. Choudhary. A fast high utility itemsets mining algorithm. 
In Proc. of the Utility-Based Data Mining Workshop in conjunction with the 11th ACM SIGKDD, 2005.
In other words, each dataset consists of two files, the transaction file and the utility file.
1) The transaction file is of the following format where every entry is a long integer: 
the number of transactions
the number of distinct items
an additional number
Tranaction-id length-of-transaction item-1 quantity-1 item-2 quantity-2  ...  
...
Tranaction-id length-of-transaction item-1 quantity-1 item-2 quantity-2  ... 
2) The utility file is of the following format where every entry is a float number:
price-of-item-1 
price-of-item-2
...
price-of-item-n
Note: 
Items are represented by an integer starting from 0, that is, 0 is item-1.

6. The parameters used in the scripts are: 
	-D 	the transaction file name
	-E 	the utility file name
	-O	the result file name
	-N	the number of items
	-W	the maximum width of a transaction
	-# 	the number of transaction
	-S	the absolute value of utility threshold
	-U	the relative value of utility threshold
	-M 	the number of transactions to be inserted in each round since Round 2
	-I	the number of transactions to be deleted in each round 
	-C	the number of rounds
	-B	the number of the transaction at the very beginning (Round 1)

	-R 		the strategy parameter: filtering unpromising items
	-F 		the strategy parameter: materialization threshold

--------------------------------------------------------------------
Thank you very much for using our algorithm. 

Junqiang Jimmy Liu
