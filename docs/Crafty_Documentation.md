Just a couple of notes about crafty/java/etc.  
Official Crafty Documentation: https://docs.craftycontrol.com  

**1. Java Versions:**  
  1.12 and below = Java 8  
  1.13+ = Java 11  
  1.17+ = Java 17  
  1.21+ = Java 21  
  Use `sudo update-alternatives --config java` to swap between installed java versions. **IMPORTANT:** The active java version MUST match the version of MC you're trying to run, if not then crashy crashy. Always verify your versions are correct.  

**2. Server Executable and Execution Command:**  
  You'll need to verify that the `Server Executable` and `Server Execution Command` fields are correct.  
  **Server Executable:** `libraries\net\minecraftforge\forge\1.20.1-47.2.0\forge-1.20.1-47.2.0-server.jar`  
  **Server Execution Command:** `java -Xms4096M -Xmx16384M @libraries/net/minecraftforge/forge/1.20.1-47.4.0/unix_args.txt nogui`  
  **ADDITIONAL NOTE:** You may need to change the file name of the executable if you have to use a different version of the Forge launcher. ALWAYS verify that the executable and execution command have the correct file path or again, crashy crashy.  
