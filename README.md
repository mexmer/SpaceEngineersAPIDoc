# Space Engineers API Doc Generator project
This is attempt to create more descriptive documentation for ModAPI and related namespaces. That might eventualy replace Docummentation.chm (or might not).

## Configuration
Project is configured to expect it's located besided SE source code. Uses relative path to source solution ..\SpaceEngineers\SpaceEngineers.sln

__Example__

* _Parent folder_ D:\Sources\Github
* _SE Source folder_ D:\Sources\Github\SpaceEngineers
* _SE Doc source folder_  D:\Sources\Github\SpaceEngineersAPIDoc

After you setup source build SE source in Release|x86 configuration, then you can build SHFB project.

### Note
I suggest to add following lines into your user.preps inside SE source folder, this will generate xmldoc, otherwise SHFB will need to disamble dlls to get proper interfaces, and you will most likely miss all comments.

 > &lt;PropertyGroup Condition=" '$(Configuration)|$(Platform)' == 'Release|x86' "&gt;
    &lt;DocumentationFile&gt;$(OutDir)\$(ProjectName).xml&lt;/DocumentationFile&gt;
  &lt;/PropertyGroup&gt;

### Comment
Feel free to contribute, since i will be doing it only in my free time.
