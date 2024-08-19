# DLL Preloading Attack

© 2022 by Innovation In Software Corporation
Stephen King wrote, “Sooner or later, everything old is new again.”
For that reason, adversaries are returning to the DLL Preloading Attack, which is a historical threat that has made a comeback.
The DLL Preloading Attack is simple to implement.

The attacker relies on probing for a dynamic link library (DLL) to launch an alternate library as a trojan. When loaded at runtime without a fully qualified name, Windows probes the location of a dynamic link library:
1. Application directory
2. System directory
3. System directory (16-bit)
4. Windows directory
5. Current directory

When the dynamic link library is launched at runtime, without the full path, the operating system will load the first similarly named library based on probing. Adversaries can leverage DLL Preloading as the first step of another vulnerability, including an Escalation of Privilege attack.
DLL Preloading attacks have been effective on a variety of well-known products, including Internet Explorer (IE7). Here is the story: https://bit.ly/3p5Kt2l