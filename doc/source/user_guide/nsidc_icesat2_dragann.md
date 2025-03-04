nsidc_icesat2_dragann.py
========================

- Acquires the [ATL03 geolocated photon height product](https://nsidc.org/data/ATL03) and appends the [ATL08 DRAGANN classifications](https://nsidc.org/sites/nsidc.org/files/technical-references/ICESat2_ATL08_ATBD_r003.pdf) from NSIDC.
- The first time we run the script, it will copy the necessary dataset in the selected local directory.
- If we already have all the data, and we run the script again: only files added or modified on the remote server will downloaded.

#### Calling Sequence
```bash
python nsidc_icesat2_dragann.py --user <username> --directory <outgoing> \
	--release 003 --granule 10 11 12 --mode 0o775
```
[Source code](https://github.com/tsutterley/read-ICESat-2/blob/main/scripts/nsidc_icesat2_dragann.py)

#### Command Line Options
- `-U X`, `--user X`: username for NASA Earthdata Login
- `-N X`, `--netrc X`: path to .netrc file for alternative authentication
- `-D X`, `--directory`: local working directory for receiving data
- `-r X`, `--release X`: ICESat-2 data release to sync
- `-v X`, `--version X:` ICESat-2 data version to sync
- `-t X`, `--track X`: ICESat-2 reference ground tracks to sync
- `-g X`, `--granule X`: ICESat-2 granule regions to sync
- `-F`, `--flatten`: Do not create subdirectories
- `-M X`, `--mode X`: Local permissions mode of the directories and files synced
- `-T X`, `--timeout X`: Timeout in seconds for blocking operations
- `-R X`, `--retry X`: Connection retry attempts
- `--log`: output log of files downloaded
- `--list`: print files to be transferred, but do not execute transfer
- `-C`, `--clobber`: Overwrite existing data in transfer
