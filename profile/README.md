# IAGA Division VI Working Group for MT Data Standards  

This group repository is a collaborative space for the working group and others to develop and communicate magnetotelluric (MT) data standards for time series, transfer functions, and models.  

The main documentation is an book created with [MyST](https://mystmd.org/) and is located here [MTH5 Documentation](https://iaga-dvi-datastandards.github.io/mth5_documentation.github.io/).

# Repositories
Within this repository are all the repositories for working with MTH5 files.  The hierarchy is

```
---------------     -----------------     ---------     --------     --------------
| mt-metadata | --> | mt-timeseries | --> | mt-io | --> | mth5 | --> | mth5-panel | 
---------------     -----------------     ---------     --------     --------------
                                                           |     ------------------
                                                           | --> | mth5-validator |
                                                                 ------------------ 
```

- [MTH5](https://github.com/IAGA-DVI-DataStandards/mth5) --> Main package for creating, manipulating, and interrogating MTH5 files. Built on [h5py](https://docs.h5py.org/en/stable/index.html).
  - [mt-io](https://github.com/IAGA-DVI-DataStandards/mt-io) --> Package for reading in various data types into `mt-timeseries` objects `ChannelTS` and `RunTS`.
  - [mt-timeseries](https://github.com/IAGA-DVI-DataStandards/mt-timeseries) --> Package for time series containers `ChannelTS` and `RunTS`.  Built on [xarray](https://docs.xarray.dev/en/stable/index.html). 
  - [mt-metadata](https://github.com/IAGA-DVI-DataStandards/mt_metadata) --> Build on [Pydantic](https://pydantic.dev/docs/validation/latest/get-started/) for fast validation.
- [MTH5 Test Data](https://github.com/IAGA-DVI-DataStandards/mth5-test-data) --> repository of test data for reading into `mt-timeseries` objects and building MTH5 files.
- [mth5-panel](https://github.com/IAGA-DVI-DataStandards/mth5-panel) --> Panel application (GUI) to create MTH5 files and plot the time series.
- [mth5-validator](https://github.com/IAGA-DVI-DataStandards/mth5-validator) --> Simple standalone validator for MTH5 files.

# How To Contribute

This is very much a community driven project so please contribute.  

## Raise an Issue

If you find something is not working, or you have a suggestion for updates please raise an issue.  If you have a general issue you can raise an issue at https://github.com/IAGA-DVI-DataStandards/.github, otherwise raise an issue in the specific repository.

## Create a Pull Request

If you would like to add functionality, fix a bug, or add documentation please clone or fork the repository you'd like to change, commit changes, push, and create a pull request.

## Join a Discussion

Feel free to raise a question on the discussion: https://github.com/orgs/IAGA-DVI-DataStandards/discussions.

## Contribute Data

For now, create a pull request in [mth5-test-data](https://github.com/IAGA-DVI-DataStandards/mth5-test-data) with example data.  Follow the current structure of `mth5-test-data` for installation and add any pertinent information.  Try to keep the data to less than a 50 Mb zip file.  We are currently working on setting up an LFS dataset.
