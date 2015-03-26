<font size='4'>
A library using 7z.dll/7z.so(from <a href='http://www.7-zip.org/'>7-Zip</a>) to handle different archive types. lib7zip is based on 7zip/p7zip source code, but <b>NOT</b> including any source code from 7zip/p7zip.<br>
</font>
<table>
<tr>
<td>
<h2>Tips</h2>
<ul><li>Build lib7zip<br>
<ul><li>Under UNIX/LINUX like system<br>
<ol><li>Get a copy of <b>p7zip</b> source code, and extract to a folder<br>
</li><li>Define a env P7ZIP_SOURCE_DIR point to the extracted folder<br>
</li><li>Call configure && make to build lib7zip library, or call autogen.sh<br>
</li></ol></li><li>Under windows<br>
<ol><li>Get mingw from <a href='http://www.mingw.org'>http://www.mingw.org</a>
</li><li>Get a copy of original <b>7zip</b> source code, <b>NOT</b> the <b>p7zip</b> for linux<br>
</li><li>Define a env P7ZIP_SOURCE_DIR point to the extracted folder<br>
</li><li>Call configure && make to build lib7zip library, or call autogen.sh<br>
</li></ol></li></ul></li><li>Run lib7zip<br>
<ul><li>Under UNIX/LINUX like system<br>
<ol><li>install <b>p7zip</b> binary<br>
</li><li>find 7z.so path, export LD_LIBRARY_PATH=<where 7z.so existing><br>
</li></ol></li><li>Under Windows<br>
<ol><li>install <b>7zip</b> binary<br>
</li><li>copy 7z.dll to where your application existing</li></ol></li></ul></li></ul>


<pre><code>   Any time or any problem about lib7zip, please feel free to write me an email.<br>
   Any feature or patch request, please also feel free to write me an email.<br>
</code></pre>

<h2>Thanks</h2>
<ul><li>Many thanks to Joe who provide so many great patches<br>
</li><li>Many thanks to Christoph who give so many great advises and patch.<br>
</li><li>Many thanks to Christoph Thielecke to provide great patches for OS2 and dynamic library</li></ul>

<h2>To Do</h2>
<ul><li>Add Compress function to library<br>
<h2>Related Projects</h2>
</li><li>Python Binding created by Mark, <a href='http://github.com/harvimt/pylib7zip'>http://github.com/harvimt/pylib7zip</a></li></ul>

<h2>Change Log</h2>
<h3>1.6.5</h3>
<ul><li>Add new parameter <b>bool fDetectFileTypeBySignature</b> to <code>OpenArchive</code>, when fDetectFileTypeBySignature = true, lib7zip will using file signature instead file name extension to detect file type<br>
</li><li>remove out-of-dated visual studio files<br>
<h3>1.6.4</h3>
</li><li>add AUTHORS COPYING file<br>
</li><li>add LIB7ZIP<code>_</code> prefix to error code enum,break the old client, please update your code<br>
</li><li>add APIs <code>SetLib7ZipLocale and GetLib7ZipLocale</code>, client could use these API to force lib7zip locale, otherwise lib7zip will use current user's locale<br>
</li><li>add list of path to find 7z.so when 7z.so is not in users ld path<br>
</li><li>fix Mac OSX compile fail problem<br>
<h3>1.6.3</h3>
</li><li>Add <code>GetLastError to C7ZipLibrary</code> and Error code define in lib7zip.h<br>
</li><li>open archive with password now work for archive created by 7za a -mhe -p, who encrypted the file names in archive<br>
<h3>1.6.2</h3>
</li><li>Fixed broken windows built system<br>
</li><li>Fixed build script for windows<br>
<h3>1.6.1</h3>
</li><li>Add OS2 support<br>
</li><li>create dynamic library along with static library<br>
<h3>1.6.0</h3>
</li><li>Add Multi-Volume support<br>
<h3>1.5.0</h3>
</li><li>Add Password support<br>
<h3>1.4.1</h3>
</li><li>Add GetProperty functions to C7ZipArchive to retrieve archive properties<br>
</li><li>Add kpidSize to return Item umcompressed size, the same as GetSize returning<br>
<h3>1.4.0</h3>
</li><li>Add patches from Christoph<br>
<ol><li>make the test program works when no Test7Zip.7z found<br>
</li></ol></li><li>Add functions to get more property about items in the archive<br>
</li><li>Tested on Mac OS X<br>
</li><li>Move source control to <a href='http://mercurial.selenic.com/'>Mercurial</a> for better distributed development<br>
<h3>1.3.0</h3>
</li><li>Add patches from Joe,<br>
<ol><li>make the library work with latest p7zip 9.20<br>
<h3>1.0.2</h3>
</li></ol></li><li>Add patches from Joe,<br>
<ol><li>Add a method to get the compressed size<br>
</li><li>Add a method to expose whether the file is encrypted<br>
</li></ol></li><li>Build scripts update<br>
</li><li>Small fix to make the lib working with the latest p7zip source<br>
<h3>1.0.1</h3>
</li></ul><ol><li>First release, support both LINUX and windows platform.<br>
</td>
<td valign='top'>
<br>
</td>
</tr>
</table>