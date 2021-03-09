# Adobe
Issues fixex

UI SCALING ISSUE IN 4K screens

> go to registry editor
> go to this path Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\SideBySide
> create a new registry DWORD (32 bit value)
> name it "PreferExternalManifest" and double click it and change to decimal and value data to '1'.
> now make a file named "photoshop.exe.manifest" and paste the following code in that file and paste that file in the folder where photoshop.exe file exist in the 
"C:\Program Files\Adobe\Adobe Photoshop CC (64 Bit)"




<?xml version="1.0" encoding="UTF-8" standalone="yes"?>

<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">

<dependency>
  <dependentAssembly>
    <assemblyIdentity
      type="win32"
      name="Microsoft.Windows.Common-Controls"
      version="6.0.0.0" processorArchitecture="*"
      publicKeyToken="6595b64144ccf1df"
      language="*">
    </assemblyIdentity>
  </dependentAssembly>
</dependency>

<dependency>
  <dependentAssembly>
    <assemblyIdentity
      type="win32"
      name="Microsoft.VC90.CRT"
      version="9.0.21022.8"
      processorArchitecture="amd64"
      publicKeyToken="1fc8b3b9a1e18e3b">
    </assemblyIdentity>
  </dependentAssembly>
</dependency>

<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
  <security>
    <requestedPrivileges>
      <requestedExecutionLevel
        level="asInvoker"
        uiAccess="false"/>
    </requestedPrivileges>
  </security>
</trustInfo>

<asmv3:application>
  <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
    <ms_windowsSettings:dpiAware xmlns:ms_windowsSettings="http://schemas.microsoft.com/SMI/2005/WindowsSettings">false</ms_windowsSettings:dpiAware>
  </asmv3:windowsSettings>
</asmv3:application>

</assembly>
