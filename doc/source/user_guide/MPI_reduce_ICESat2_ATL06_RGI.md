MPI_reduce_ICESat2_ATL06_RGI.py
===============================

- Create masks for reducing ICESat-2 data to the [Randolph Glacier Inventory](https://www.glims.org/RGI/rgi60_dl.html)

#### Calling Sequence
```bash
mpiexec -np <processes> python3 MPI_reduce_ICESat2_ATL06_RGI.py <path_to_ATL06_file>
```
[Source code](https://github.com/tsutterley/read-ICESat-2/blob/main/scripts/MPI_reduce_ICESat2_ATL06_RGI.py)

#### Inputs
1. `ATL06_file`: full path to ATL06 file

#### Command Line Options
- `-D X`, `--directory X`: Working data directory for the Randolph Glacier Inventory
- `-R X`, `--region X`: region number of Randolph Glacier Inventory to run
    1. Alaska
    2. Western Canada and USA
    3. Arctic Canada North
    4. Arctic Canada South
    5. Greenland Periphery
    6. Iceland
    7. Svalbard
    8. Scandinavia
    9. Russian Arctic
    10. North Asia
    11. Central Europe
    12. Caucasus, Middle East
    13. Central Asia
    14. South Asia West
    15. South Asia East
    16. Low Latitudes
    17. Southern Andes
    18. New Zealand
    19. Antarctic, Subantarctic
- `-V`, `--verbose`: output module information for process
- `-M X`, `--mode X`: permissions mode of output HDF5 datasets
