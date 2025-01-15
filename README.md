# halld_daq_rcdb
Collection of scripts for HallD DAQ RCDB 

## Install to CDAQ

As of beginning of 2025 it looks like this: 

1. Clone https://github.com/JeffersonLab/halld_daq_rcdb.git
2. clone rcdb versions you need into it
3. Make a symbolic link `rcdb_current` to this directory
4. All scripts assume the current version of rcdb is `rcdb_current` and point to it


```bash
# Clone halld rcdb scripts. We name it rcdb to confuse everyone
git clone https://github.com/JeffersonLab/halld_daq_rcdb.git rcdb
cd rcdb

# Note we use shallow clone for 
git clone https://github.com/JeffersonLab/rcdb.git -b v2.0.0 --depth 1 rcdb_v2.0.0

# Unlink previous rcdb_current if exists
unlink rcdb_current

# Set RCDB v2.0.0 as current: 
ln -s rcdb_v2.0.0 rcdb_current
```

