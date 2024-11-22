# Envy BBS Documentation

## Configuration Files
### envy.ini

`envy.ini` lives in your BBS's working directory, it is used both by servo and envy.

 * Main Section
   * **telnet port** Port to listen for telnet connections on
   * **max nodes** Maximum number of nodes (similtanious connections)
   * **default tagline** Default tagline for networked message bases, can be overridden.
   * **sysop name** The username belonging to the Sysop
   * **bbs name** The name of your bbs
 * Path Section
   * **gfile path** Path to where gfiles are located (Relative to working directory)
   * **data path** Path to where data files are (Relative to working directory)
   * **message path** Path to where message base data is stored (Relative to working directory)
   * **log path** Path where to store log files (Relative to working directory)
   * **temp path** Base path for temporary files eg. Drop files (Relative to working directory)
   * **scripts path** Path to where the JavaScript scripts live (Relative to working directory)
  
### msgbases.toml

### doors.toml

### seclevels.toml

### trashcan.txt

## Javascript Reference

...
