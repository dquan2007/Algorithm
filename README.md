# Algorithm

Algorithm is an open source code and provides a series of relatively independent algorithm libraries, and you can use one or a few required libraries individually.

All algorithms are completed on the windows platform, based on the visual studio 2019 community edition.

## Configuration

Firstly, you need to complete the changes to the default project configuration of visual studio 2019. The default project configuration file is in the installation directory, which is generally located at `C:\Program Files(x86)\Microsoft Visual Studio\2019\Community\Common7\IDE\VC\VCWizards\default.vcxproj`. Follow the tips below to add content, then you can create the required libraries according to the default configuration.

```xml
<PropertyGroup Label="UserMacros" />
<!-- The previous content remains the same -->
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|Win32'">
    <OutDir>.\..\$(Configuration)\$(Platform)\$(PlatformToolset)\</OutDir>
    <IntDir>.\..\$(Configuration)\$(Platform)\$(PlatformToolset)\$(ProjectName)\</IntDir>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|x64'">
    <OutDir>.\..\$(Configuration)\$(Platform)\$(PlatformToolset)\</OutDir>
    <IntDir>.\..\$(Configuration)\$(Platform)\$(PlatformToolset)\$(ProjectName)\</IntDir>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|x64'">
    <OutDir>.\..\$(Configuration)\$(Platform)\$(PlatformToolset)\</OutDir>
    <IntDir>.\..\$(Configuration)\$(Platform)\$(PlatformToolset)\$(ProjectName)\</IntDir>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|Win32'">
    <OutDir>.\..\$(Configuration)\$(Platform)\$(PlatformToolset)\</OutDir>
    <IntDir>.\..\$(Configuration)\$(Platform)\$(PlatformToolset)\$(ProjectName)\</IntDir>
  </PropertyGroup>
<!-- Later content remains the same -->
<PropertyGroup />
```

Secondly, you need to add the system environment variable VSHOME, whose value is the IDE directory of visual studio 2019, which is generally located at `C:\Program Files(x86)\Microsoft Visual Studio\2019\Community\Common7\IDE\`.

At last, you can modify the template files of the header file and the source file, such as adding copyright and comment information etc. to the file header. The template file of the header file is generally located at `C:\Program Files(x86)\Microsoft Visual Studio\2019\Community\Common7\IDE\VC\vcprojectitems\hfile.h`, and the template file of the source file is generally located at `C:\Program Files(x86)\Microsoft Visual Studio\2019\Community\Common7\IDE\VC\vcprojectitems\newc++file.cpp`.

## Structure

### Publish

This directory stores published library packages. These libraries may be custom libraries or libraries compiled from free open source code.

See the link for more information: [Published library packages](Publish/README.md)

### Library Items

This directory stores the source code of all library projects.

See the link for more information: [Library items](LibraryItems/README.md)

### Tools

This directory stores some tools that are convenient for project management and use.

See the link for more information: [Tool list](Tools/README.md)

## References

* [OpenCASCADE](https://www.opencascade.com/content/open-source-core-technology)
* [Google Test](https://github.com/google/googletest)
* [TinyXML-2](https://github.com/leethomason/tinyxml2)
* [SVGnest](https://github.com/Jack000/SVGnest)
* [LinuxCNC](https://github.com/LinuxCNC/linuxcnc)

