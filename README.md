gr-cdma
=======

This is the gr-cdma out-of-tree package.
To use the cdma blocks, the Python namespaces
is in 'cdma', which is imported as:

    import cdma

See the Doxygen documentation for details about the blocks available
in this package. A quick listing of the details can be found in Python
after importing by using:

    help(cdma)

For the impatient:

1) Download gr-cdma from github
> git clone https://github.com/anastas/gr-cdma.git

2) Build the package
> mkdir build_cdma

> cd build_cdma

> cmake -DENABLE_DOXYGEN=ON ../gr-cdma

> make

> sudo make install

> sudo ldconfig


3) compile hierarchical blocks and play with built in app
> cd gr-cdma/apps

> gnuradio-companion &

In the gnuradio-companion environment

-- Load the hier block "amp_var_est_hier.grc", "cdma_tx_hier.grc", "chopper_correlator1.grc", "cdma_rx_hier.grc" and compile them

-- Reload all blocks in grc

-- Load the application "cdma_txrx.grc" and have fun

   Experiment with manual acq/tra, auto acq/tra, changing freq and timing offset, SNR, etc

-- If you have 2 USRPs load the cdma_tx.grc and cdma_rx.grc and enjoy real-time CDMA transmission. You can also use the cdma_tx.grc and cdma_rx.grc by writting
and reading to a fifo (first do > makefifo /tmp/cdma.fifo)
