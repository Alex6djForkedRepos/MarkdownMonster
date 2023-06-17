### Bugs and Needed Features

* [ ] Fix Pipe Table Import/Format

* [ ] Fix Simple Editor - Copy/Paste operations not working (menu)
* [ ] Gist Addin - Fix Refresh in Previewer
* [ ] Allow saving documents as admin when permissions fail
* [ ] mmCLI: Enable Windows Long Path Support (win10)
navigating~~
* [x] ~~Image File Drag and Drop no longer works~~

#### Enhancements
* [ ] GitHub Dark Theme
* [ ] Open Files List from Command Palette

### Nice to Have
* Conversion .NET Core 6.0  
	* Issues:
		* `ExcecuteScript()` functionality
		* use of `dynamic` fixes
		* Figure out Runtime Distribution

### Consideration
* [ ] Markup (Publishing) support
* [ ] reveal.js presentations as an Addin
* [ ] FTP Upload Addin (started)



### Markdown Monster .NET CORE 6.0 Migration

**Issues**

* .NET Framework Assemblies that require updates
	* XmlRpc  
	  *(fails to load in Core)*
	* Windows Speech Engine (not supported for .NET Core)  
	  *(conditionally removed for Core)*
	  *Found explicit library that can be shipped from NuGet*

	* Wpf.FontAwesome  
	  *(apparently works with net462 binary)*
	* HUnspell (fixed with ported version)
	  *(apparently works with net462 binary)*
	  
* Pathing Resolution issues 
	* Weird File not Found errors  
	*(file not found errors in Folder Browser and other places)*
	* Addins and binary files dump into output folder
	* ~~GoUrl() with filename breaking on paths with spaces (fixed)  
	  *(due to change in default of ShellExecute in ProcessInfo)*~~
	 