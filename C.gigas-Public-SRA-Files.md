### SRA Acquisition
For efficiency, all SRA files were downloaded directly to our server via Study Number using the command-line program "wget", instead of downloading each SRA file individually.

Study Numbers for Crassostrea gigas SRA files were systematically identified and downloaded in the following fashion:

1. Searched NCBI SRA database with "Crassostrea gigas"

2. Obtained the HTTP link to download all files in the corresponding Study Number:

 2a. Clicked Run number.

 2b. Clicked the "Download" tab.

 2c. Copied the HTTP link next to the Study Number
 
3. Used HTTP link in Step 2c in wget command to download files directly to server.

4. Searched NCBI SRA database using "Advanced Search" to exclude the Study Number(s) previously downloaded.

5. Return to Step 2.



Example wget command for retrieving SRA files via Study Number:

    wget -r -no-check-certificate --reject="index.html" --secure-protocol=auto -e robots=off --wait=10 http://ftp-trace.ncbi.nlm.nih.gov/sra/sra-instant/reads/ByStudy/sra/SRP/SRP029/SRP029373/

