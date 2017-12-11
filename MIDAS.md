<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#org7c68ca9">1. Switching over to MIDAS</a></li>
</ul>
</div>
</div>


<a id="org7c68ca9"></a>

# Switching over to MIDAS

1.  Hardware

    -   Take veto (O1) out of VM-USB module in VME crate
    -   Plug the twisted pair cable into veto of ADC (red on top)

2.  Software

    1.  General Notes:
    
        -   Data is saved in  `/home/daq/midas/online`
            -   link points to `/data/midas/data`
        -   Run files saved at `v785` (symbolic link)
        -   v785 points to specific directory (eg. `/2017-11-14_DAQTests`)
        -   Actual DAQ code is in `/home/daq/midas/online/src/v785`
            -   'v785' is the experiment name
    
    2.  Starting the DAQ
    
        -   See what experiment is active
            
                echo $MIDAS_EXPT_NAME
        -   If it's not 'v785', do this:
            
                export MIDAS_EXPT_NAME=v785
        -   Move into the experiement directory
            
                cd /home/daq/midas/online/src/v785
        -   To start the DAQ
            
                ./start_daq.sh
            
            The analyzer should pop up (there may be a couple of errors but
            ignore them)
        -   Open google chrome
            -   Click on MIDAS bookmark
            -   If there's an error about security, go to Advanced -> proceed anyway
            -   Username: daq
            -   Password: the usual ;)
            -   Click on "EngeRun" to go to the Enge-specific run page
            -   Click on "ODB" at the top
            -   Click on "Run info"
            -   Click on "Run Number", set to zero if this is a new experiment
        -   

