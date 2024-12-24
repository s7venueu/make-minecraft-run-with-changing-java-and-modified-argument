This is a guide/tips to tune Java for Minecraft.
(TestedByMyself)

Requirement
======


- [**Oracle GraalVM**](https://www.graalvm.org/downloads/) features a more aggressive Java compiler. (download version 23 or latest but now I am using version 23)
  
 **1.** Change to the directory where you to install GraalVM, then extract the .zip to **```C:\Program Files\Java```**
 
 **2.** There can be multiple JDKs installed on the machine. The next step is to configure the runtime environment. Setting environment variables via the command line (```Run CMD as a Administrator```) will work the same way for Windows.
Set the JAVA_HOME environment variable to resolve to the GraalVM installation directory.

:
**```setx /M JAVA_HOME "C:\Program Files\Java\graalvm-jdk-23.0.1+11.1"```**

 **3.** Set the value of the PATH environment variable to the GraalVM bin directory
 
 : 
 **```setx /M PATH "C:\Program Files\Java\graalvm-jdk-23.0.1+11.1"```**

 
**4.** Restart Command Prompt to reload the environment variables. Then use the following command to check whether the variables were set correctly:

 **```echo %PATH```**
 
**```echo %JAVA_HOME%```**

***Alternatively***, you can set up environment variables through a Windows GUI:

 **1.** Go to Windows Start Menu, then Settings, then Advanced.
 
 **2.** Click Environment Variables. In the section “System Variables” find the JAVA_HOME variable and select it 
 
 **3.** Click Edit.
 
 **4.** Click New.
 
 **5.** Click Browse to find the directory to add. Confirm by clicking OK.
 
 **6.** Restart the Command Prompt to reload the environment variables.

Modified Java Argument (GraalVM)
 ======


 This flag can used on java GraalVM 23+ :

 ```-XX:+UnlockExperimentalVMOptions -XX:+UnlockDiagnosticVMOptions -XX:+AlwaysActAsServerClassMachine -XX:+ParallelRefProcEnabled -XX:+AlwaysPreTouch -XX:+DisableExplicitGC -XX:+UseNUMA -XX:AllocatePrefetchStyle=3 -XX:NmethodSweepActivity=1 -XX:ReservedCodeCacheSize=400M -XX:NonNMethodCodeHeapSize=12M -XX:ProfiledCodeHeapSize=194M -XX:NonProfiledCodeHeapSize=194M -XX:+PerfDisableSharedMem -XX:+UseFastUnorderedTimeStamps -XX:+UseCriticalJavaThreadPriority -XX:+EnableJVMCI -XX:+UseJVMCICompiler -XX:+EagerJVMCI -XX:JVMCIThreads=8 -XX:+EnableVectorSupport -XX:+UseCompressedOops -XX:+AlignVector -XX:+OptoBundling -XX:+OptimizeFill -XX:+AlwaysCompileLoopMethods -XX:+EnableVectorAggressiveReboxing -XX:+OptoScheduling -XX:+UseCharacterCompareIntrinsics -XX:+UseCopySignIntrinsic -XX:+UseVectorStubs -Dgraal.UsePriorityInlining=true -Dgraal.TuneInlinerExploration=1 -Dgraal.PrintCompilation=true -Dgraal.CompilerConfiguration=community -Dgraal.Vectorization=true -Dgraal.OptDuplication=true -Dgraal.DetectInvertedLoopsAsCounted=true -Dgraal.LoopInversion=true -Dgraal.VectorizeHashes=true -Dgraal.EnterprisePartialUnroll=true -Dgraal.VectorizeSIMD=false -Dgraal.StripMineNonCountedLoops=true -Dgraal.SpeculativeGuardMovement=true -Dgraal.InfeasiblePathCorrelation=true -Dfml.ignoreInvalidMinecraftCertificates=true -Dfml.ignorePatchDiscrepancies=true -Djava.net.preferIPv4Stack=true```

if you use shaders,make sure for this code is false like this ```-Dgraal.VectorizeSIMD=false``` 

but if you not use shaders change the code to be ```-Dgraal.VectorizeSIMD=true``` 



 i will give some example for changing java selection and argument **(i used cracked minecraft & dont buy original app lol)**
 ======

 ****TLauncher****

 **1.** Open your launcher and go to settings

 **2.** then you select change
 
![Screenshot 2024-12-24 022854](https://github.com/user-attachments/assets/62b22106-8486-42f6-b596-657f335152c5)

**3.** now click browse to select java what will you use (GraalVM), find where you path that app and click open

![Screenshot 2024-12-24 022938](https://github.com/user-attachments/assets/aaf0d625-e8f5-40c6-87f6-36b9cdb5fcb9)  ![Screenshot 2024-12-24 022955](https://github.com/user-attachments/assets/d01a89a4-969a-412f-8e70-6783fea16a9f)

**4.** Delete all text on 'JAVA Arguments' and replace it

![Screenshot 2024-12-24 023025](https://github.com/user-attachments/assets/be30be53-5923-4956-b244-38b15c20021a)

**5.** save and change java selection

![Screenshot 2024-12-24 023042](https://github.com/user-attachments/assets/54300668-874e-49b4-a171-2239d1e31f4e)



**If you Wanna get more fps on your minecraft use combo fabric,iris,sodium & SimplyOptimized**
======

**Fabric** :https://fabricmc.net/

**Sodium** :https://modrinth.com/mod/sodium/versions

**Iris**   :https://modrinth.com/mod/iris

**SimplyOptimized** : https://modrinth.com/modpack/sop (you need to know how to install it)


SOURCES
======

(https://github.com/brucethemoose/Minecraft-Performance-Flags-Benchmarks)




 
