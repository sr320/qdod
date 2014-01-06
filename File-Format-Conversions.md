Examples of queries that will convert between standard file formats
<hr>
### methratio (BSMAP) to GFF

```
SELECT 
chr as seqname,  
'methratio' as source,  
'CpG' as feature, 
pos as start,
pos + 1 as [end],
ratio as score,  
strand,  
'.' as frame,  
'.' as attribute

FROM [sr320@washington.edu].     
[BiGO_betty_plain_methratio_v1.txt] betty 
where 
context like '__CG_' --_=single character wildcard
and
CT_Count > 9
```
Explanation:
<hr>
### methratio (BSMAP) to IGV

```
SELECT 
chr as seqname,  
pos - 1 as start, -- compensating for going to zero-based
pos + 1 as [end], 
'CG' as feature, 
ratio as score

FROM [sr320@washington.edu].     
[BiGill_methratio_v9_A.txt] yel 
where 
context like '__CG_' --_=single character wildcard
and
CT_Count >= 5​
```
Explanation:
<hr>

###Methratio outputs to format needed for methylKit in SQLShare

```
SELECT 
  chr as chr,
  pos as start,
  '+' as strand,
  cast (CT_count as float) as CT_count,
  cast (C_count as float) as C_count,
  cast (C_count as float) / cast (CT_count as float) as freqC,
  1 - (cast (C_count as float) / cast (CT_count as float)) as freqT
  
FROM [sr320@washington.edu].[BiGill_methratio_v9_A.txt]
  where 
context like '__CG_'
and
  CT_Count >= 5 
and 
  ratio <> 'NA'
```
--

Python client formatted    

```
python /Users/sr320/sqlshare-pythonclient/tools/fetchdata.py -s "SELECT chr as chr, pos as start, '+' as strand, cast (CT_count as float) as CT_count, cast (C_count as float) as C_count, cast (C_count as float) / cast (CT_count as float) as freqC, 1 - (cast (C_count as float) / cast (CT_count as float)) as freqT FROM [sr320@washington.edu].[BiGo_lar_T1D3] where context like '__CG_' and CT_Count >= 5 and ratio <> 'NA'" -o /Volumes/web/cnidarian/BiGo_lar_T1D3_methylkit_input.csv
```

###Hack for later join

```
SELECT 
  chr + '_' + (cast (pos as varchar)) as chr_start,
  chr as chr,
  pos as start,
  '+' as strand,
  cast (CT_count as float) as CT_count,
  cast (C_count as float) as C_count,
  cast (C_count as float) / cast (CT_count as float) as freqC,
  1 - (cast (C_count as float) / cast (CT_count as float)) as freqT
  
FROM [sr320@washington.edu].[BiGo_lar_M1]
  where 
context like '__CG_'
and
  CT_Count >= 5 
and 
  ratio <> 'NA'​​​​​
```

python code
```python
!python /Users/sr320/sqlshare-pythonclient/tools/fetchdata.py -s "SELECT chr + '_' + (cast (pos as varchar)) as chr_start, chr as chr, pos as start, '+' as strand, cast (CT_count as float) as CT_count, cast (C_count as float) as C_count, cast (C_count as float) / cast (CT_count as float) as freqC, 1 - (cast (C_count as float) / cast (CT_count as float)) as freqT FROM [sr320@washington.edu].[BiGo_lar_M1] where context like '__CG_' and CT_Count >= 5 and ratio <> 'NA'" -f tsv -o /Volumes/Monarch/cnidary/BiGo_lar_M1_methylkit4_input.txt
```