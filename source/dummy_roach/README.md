This class is used to simulate a ROACH connection. Use when you want to test scripts but don't want to connect to a real ROACH board. 

For simplicity any function that returns data will return an array of zeros. The only function that I was unable to replicate correctly is the `snapshot_get` function. That is because the size of the array returned by this function is dependant of the model loaded by the ROACH, so it can't be predicted beforehand. In this case, the class an array of 256 zeros as byte string (the default of the get plot_snapshots script).

Note: I only implemented the functions that are used in this package. If you want to add more functions from corr's FpgaClient, you can implement them yourself.
