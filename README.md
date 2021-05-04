# azure-blob-storage-filecoin
Process Azure Blob Storage and store it in Filecoin

- Scans directory provided, and sends each file to filecoin
- Currently runs 'headless'
- Fully asynchronous
- Uses ceramic/textile libraries
- Requires a local running ipfs, powergate and lotus node (dockre instance from Slingshot excercise used in the first instance)
- For live use will require a filecoin account with significant balances to store large media
- Results are sent to console. Should be run and piped to a specified file (necessary to record cids for later recovery).
- Working prototype, not a finished and polished product
- Requires development of full error handling and logging

TODO:
- Receive final acknowledgement of 'burn' to chain, and replace local file contents with the cid and id of the storage miner (for retreival)
- Send results to log file instead of console
- Add ability to reverse process (recover contents of file based on the cid and miner id).
