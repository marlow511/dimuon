# dimuon

## Overview
This is a relatively simple example that shows how to read a nanoAOD file 
using a PyROOT script.   Additional information on PyROOT can be found 
here:  https://root.cern.ch/doc/master/group__tutorial__pyroot.html 
Additional information on the nanoAOD data format can be founds here:
https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookNanoAOD

## Setup environment

This script runs from a CMSSW environment.  To create such an environemnt,
follow the instructions here.
https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookSetComputerNode#CreateWork

## Install the script
To setup the script starting from your CMSSSW_X_X_X directory do

> cd python
> git clone https://github.com/marlow511/dimuon 
> dimuon
> cmsenv 

## Running the script

The script takes one input file, named inFile.root, which is assumed to
be in nanoAOD format. 

### PICScie
On the PICSciE system, a sample file can be
found on the mass storage system at : 
/tigress/marlow/tigress-hsm/dimuon/DoubleMu_2.root

To use this file, one can either create a Unix soft link between
this file and inFile.root, i.e., by using

> ln -s /tigress/marlow/tigress-hsm/dimuon/DoubleMu_2.root inFile.root

Alternately, the dimuon.py script can be changed to read from this
file directly.

### cmslpc

On the CMS LPC system, a sample input file can be found at:
/uscms_data/d2/marlow/CMSSW_10_2_9/src/dimuon/inFile.root

Alternately, one can copy a file from the grid using a command
like

> xrdcp root://cms-xrd-global.cern.ch//store/data/Run2016B/DoubleMuon/NANOAOD/05Feb2018_ver2-v1/80000/386897D3-530C-E811-9E5F-001E675A69DC.root inFile.root

Be careful with this, however.   These are large files!


