# GNSS_Lab-Lab5

This is a module that takes GNSS timeseries files.

There are 4 functions

1. fit_timeseries(tlist,ylist)
   tlist: time array
   ylist: y-data array
  returns velocity, and uncertainty

2. fit_velocities(filename,tname,ename,nname,uname), returns a dataframe.
  tname: header name for your time data
  ename: east-velocity component header name
  nname: north velocity component header name
  uname: up velocity component headername
  uses fit_timeseries to obtain output data
  returns a dataframe of all fit-velocities and uncertainties

3. get_coordinates(filename,lat,lon,elev), returns a dataframe
  lat: latitude header name
  lon: longitude header name
  elev: elevation/height header name

4. fit_all_velocities(folder, pattern, tname, ename, nname, uname, lat, lon, elev):
  uses fit_velocities and get_coordinates for multiple files at once using a glob pattern
  
