# Space Engineers API Doc Generator

## Configuration
Project is configured to expect it's located besided SE source code. Uses relative path to source solution ..\SpaceEngineers\SpaceEngineers.sln
**Example**
*Parent folder* D:\Sources\Github
*SE Source folder* D:\Sources\Github\SpaceEngineers
*SE Doc source folder*  D:\Sources\Github\SpaceEngineersAPIDoc

After you setup source build SE source in Release|x86 configuration, then you can build SHFB project.

### Comment
I suggest to add following lines into your user.preps inside SE source folder, this will generate xmldoc, otherwise SHFB will need to disamble dlls to get proper interfaces, and you will most likely miss all comments.

 > &lt;PropertyGroup Condition=" '$(Configuration)|$(Platform)' == 'Release|x86' "&gt;
    &lt;DocumentationFile&gt;$(OutDir)\$(ProjectName).xml&lt;/DocumentationFile&gt;
  &lt;/PropertyGroup&gt;

