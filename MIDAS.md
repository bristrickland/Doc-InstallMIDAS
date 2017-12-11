<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#orga13b792">1. Switching over to MIDAS</a></li>
</ul>
</div>
</div>


<a id="orga13b792"></a>

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
            -   `v785` is the experiment name

