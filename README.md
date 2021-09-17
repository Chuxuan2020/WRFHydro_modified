# Modify WRF-Hydro Source Code to Output Overland Flow

This is a readme file containing instructions to modify the WRF-Hydro source code to output overland flow at terrain routing grids.

## Content in this directory
1) Modified Fortran source code
module_HYDRO_io.F   
module_NWM_io.F
module_NWM_io_dict.F   
Noah_distr_routing.F
2) README.md  % the file you are reading

## How to use them?
1) Download and copy the four Fortran files to your WRF-Hydro directory that stores the source code under /$your_WRFHydro_directory$/trunk/NDHMS/Routing/
to substitute the existing files there.
2) Compile and configure WRF-Hydro following https://ral.ucar.edu/sites/default/files/public/HowToBuildandRunWRF-HydroV5inStandaloneMode.pdf
3) Copy the updated wrf_hydro.exe under RUN/ to the directory you plan to run WRF-Hydro
4) Run WRF-Hydro as you normally do and the Q_SFCFLX_X and Q_SFCFLX_Y with unit of m^3/s will be stored in the *RTOUT* output files. 
