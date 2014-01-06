
This is the website
`https://sqlshare.escience.washington.edu`
<hr>
<img src="http://eagle.fish.washington.edu/cnidarian/skitch/SQLShare_187B106E.png" alt="SQLShare_187B106E.png" width = 75%/>
<hr>

All you need to log on is a UW Id or Google Account. 

Once you log in the main UIs include

<hr>
<img src="http://eagle.fish.washington.edu/cnidarian/skitch/SQLShare_and_README.md_and_SQLShare_187B110A.png" alt="SQLShare_and_README.md_and_SQLShare_187B110A.png" width = 75%/>
<hr>
<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Upload_File_187B115D.png" alt="Upload_File_187B115D.png" width = 75%/>
<hr>
<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Upload_File_187B1184.png" alt="Upload_File_187B1184.png" width = 75%/>
<hr>

In short, SQLShare is a easy way to manipulate tabular data, including (but not limited to)    
- selecting data subsets   
- joining tables   
- performing arithmatic   
- reorganizing tabular data   

<hr>
Here is a straight-forward example of joining two tables. 
A BLAST output table will be joined with gene descriptions.

Table 1 is a BLAST output tablular file uploaded using wizard shown above.
<https://sqlshare.escience.washington.edu/sqlshare/#s=query/wearh%40washington.edu/Oly_Blast_uniprot_swissprot.txt>
<hr>
<img src="http://eagle.fish.washington.edu/cnidarian/skitch/SQLShare_-_View_Query_187B13C2.png" alt="SQLShare_-_View_Query_187B13C2.png" width = 75%/>
<hr>
<img src="http://eagle.fish.washington.edu/cnidarian/skitch/SQLShare_-_View_Query_and_SQLShare_187B14E1.png" alt="SQLShare_-_View_Query_and_SQLShare_187B14E1.png" width = 75%/>
<hr>
<img src="http://eagle.fish.washington.edu/cnidarian/skitch/SQLShare_-_View_Query_187B18DE.png" alt="SQLShare_-_View_Query_187B18DE.png" width = 75%/>
<hr> 
This can also be done in New Query UI
<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Run_Query_187B1988.png" alt="Run_Query_187B1988.png" width = 75%/>    
And from here you can Save or simply download the joined table.
<hr>



Explanation of code

```
SELECT *    
FROM     
[wearh@washington.edu].[Oly_Blast_uniprot_swissprot.txt]blast   
Left Join 
[samwhite@washington.edu].[UniprotProtNamesReviewed_yes20130610]unp 
on
blast.Column3 = unp.SPID​
```

<img src="http://eagle.fish.washington.edu/cnidarian/skitch/Run_Query_187B1B37.png" alt="Run_Query_187B1B37.png" width = 100%/>


