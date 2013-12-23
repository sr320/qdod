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

Code explanation:

wget - Starts wget program.

-r - Tells wget to download files recursively (i.e. maintaining directory structure).

-no-check-certificate - Tells wget to not check the NCBI server's security certificate.

--reject="index.html" - Tells wget to not download any files titled: index.html

--secure-protocol=auto - Tells wget to decide to use a secure connection to the NCBI server.

-e robots=off - Tells wget to ignore the "robots.txt" file on the server. The "robots.txt" file prevents webcrawlers from using too many server resources, which wget normally respects.

--wait=10 - Tells wget to wait 10 seconds between each attempt to retrieve files.  This reduces load on the NCBI server.
