### Hi there 👋

<!--
**smodic/smodic** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

After downloading the above file, we can execute SMODIC by the following commands
./SMODIC < option1 > < modelfile > < option2 > < formula >

Option1 specifies the input file of SMODIC:
-M: the input is a SM-PDS model.
-B: the input is a binary program

Option2 specifies the model checking strategy:
-L: use the LTL model checking algorithm
-C: use the CTL model checking algorithm
-R1: perform the Reachability Analysis using pre*
-R2: perform the Reachability Analysis using post*

The model file can be either a program or a SM-PDS (.smpds file). The output have three files: one for the Control Flow Graph, one for assembly codes, and one for the generated SM-PDS. A SM-PDS consists of four parts: a finite set of standard PDS transition rules, a finite set of self-modifying transition rules, an initial phase (the initial set of transition rules) and an initial configuration (initial control location equipped with the stack contents).
In order to show this, we will use the following command to check whether the program cmd.exe can eventually call the API function GetModuleA or not. For this case, we execute the following command:
./SMODIC B cmd.exe L "< > getmodulea"
