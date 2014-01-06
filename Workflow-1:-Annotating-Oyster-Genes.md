This workflow will take focus on taking a simple SQLShare table that has gene IDs and associated expression data and will take you through the steps of figuring out the name, function, etc of each gene.

---

### Initial Data Table: Oyster larvae RNA-seq - OsHV exposure


SCREENSHOT   

<img src="https://www.evernote.com/shard/s10/sh/00190b6c-beab-49f1-b22d-d5fc0f934e06/c1e5e385321f7eec2252112f8e9d0eba/deep/0/SQLShare%20-%20View%20Query.png" alt="SQLShare%20-%20View%20Query" />

---

<https://sqlshare.escience.washington.edu/sqlshare#s=query/sr320%40washington.edu/solid0078_20091105_RobertsLab_GE_F3%20trimmed%20RNA-Seq.txt>

---
### Join with [qDOD Cgigas Gene Descriptions (Swiss-prot)](https://sqlshare.escience.washington.edu/sqlshare#s=query/sr320%40washington.edu/qDOD%20Cgigas%20Gene%20Descriptions%20(Swiss-prot)



    Select * from
    [sr320@washington.edu].[solid0078_20091105_RobertsLab_GE_F3 trimmed RNA-Seq.txt]oshv
    left join
    [sr320@washington.edu].[qDOD Cgigas Gene Descriptions (Swiss-prot)]des
    on oshv.ID = des.CGI_ID
 

<https://sqlshare.escience.washington.edu/sqlshare#s=query/sr320%2540washington.edu/Cgigas%20Larvae%20RNA-Seq%20OsHV&q=>
  ​
---

### Identifying Expressed Genes Enriched in the Dataset   


```sql
Select * from
[sr320@washington.edu].[solid0078_20091105_RobertsLab_GE_F3 trimmed RNA-Seq.txt]oshv
left join
[sr320@washington.edu].[qDOD Cgigas Gene Descriptions (Swiss-prot)]des
on oshv.ID = des.CGI_ID
  
​where UniqueReads >=10​
```

<https://sqlshare.escience.washington.edu/sqlshare#s=query/sr320%40washington.edu/Cgigas%20Larvae%20RNA-Seq%20OsHV%20UR10>

---
Download file. Corresponding non-redundant SPIDs @
<http://eagle.fish.washington.edu/cnidarian/OsHV_larvae_RNAseq_UR10.txt>

---
### Joining with GO information (option 1)
Joining <https://sqlshare.escience.washington.edu/sqlshare#s=query/sr320%40washington.edu/Cgigas%20Larvae%20RNA-Seq%20OsHV%20UR10> with <https://sqlshare.escience.washington.edu/sqlshare#s=query/sr320%40washington.edu/qDOD_Cgigas_GO_GOslim_DISTINCT>   

    SELECT * 
    FROM [sr320@washington.edu].[Cgigas Larvae RNA-Seq OsHV UR10]ur
    left join
    [sr320@washington.edu].[qDOD_Cgigas_GO_GOslim_DISTINCT]ds
    on
    ur.ID = ds.CGI_ID
​

    SELECT DISTINCT
    ID,
    SPID1,
    GOID,
    term,
    aspect
    FROM [sr320@washington.edu].[Cgigas Larvae RNA-Seq OsHV UR10]ur
    left join
    [sr320@washington.edu].[qDOD_Cgigas_GO_GOslim_DISTINCT]ds
    on
    ur.ID = ds.CGI_ID
​