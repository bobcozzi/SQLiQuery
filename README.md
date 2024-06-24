# SQLiQuery
<b>SQL iQuery</b> for IBM i *SAVF download image
Licensed Program 2COZ-IQ8 
<p>It is a Web, CL and Interactive SQL query tool for IBM i, replacing the legacy Query/400 and provides an SQL/RPG style scripting langauge for more powerful queries.</p>
With SQL iQuery you can run SQL in any of the following environments:</p>
<ul><li>Command Entry</li><li>HTML/Javscript Web pages</li><li>CL programs</li><li>menus</li><li>the job scheduler</li>
<li>batch jobs</li></ul>
<h2>Download and Installation Instructions</h2> 
<p>To download SQL iQuery for IBM i <b>V7R3</b> and later <a alt="SQL iQuery *SAVF for IBM i V7R3 and later"<a href="https://www.dropbox.com/scl/fi/jw6ynqyks47h9rdtecn5v/IQUERY.zip?rlkey=n8pt6jm8mttvgl3yyqtunuhtw&dl=1">click here for IBM i v7r3+ build</a></p>
<p>To download SQL iQuery for IBM i <b>V7R2</b> and later <a href="https://www.dropbox.com/scl/fi/6es3zlfe7jltgk223522a/IQUERY72.zip?rlkey=rn7o5l1wq4lby7czol5gvlkt0&dl=1">click here for IBM i v7r2 build</a></p>
<p><a href="https://www.dropbox.com/scl/fi/3si0yp2cwgrbteggyzt66/SQL-iQuery-Script.pdf?rlkey=rpbod94h8syocrgg55w17umbj&dl=1">SQL iQuery Script Reference Manual (in development)</a></p>
<p>Existing SQL iQuery customers can update to this version at no charge. It contains bug fixes and minor enhancements over prior versions.<p>
<h4>Service, Support and Training</h4>
  <p>While SQL iQuery is completely free, users may request support, enhancements, training and local user group (LUG) lectures for a reasonable fee. 
    Send a <a href="mailto:bob@sqliquery.com?subject=SQL%20iQuery%20paid%20support%20request&body=Bob%2C%0AI%20have%20an%20SQL%20iQuery%20support%20question.%20Please%20provide%20a%20Quote%20for%20Support%20for%20the%20following%20issue%3A%0A--Insert%20your%20support%20question%20here--%0A%0AThank%20you%0A">request for support</a> to Bob Cozzi or contact him on <a href="https://www.linkedin.com/in/bob-cozzi-32432510/?lipi=urn%3Ali%3Apage%3Ad_flagship3_feed%3BCcq9zKB8QAWi%2FCSH5ZAvUg%3D%3D">LinkedIn</a> for more information.</p>
<h3>Installation Instructions</h3>
<p>After you download the iQuery.savf save file, it must be uploaded to your IBM i operating system server. You can do that using FTP binary transfer from Windows, Mac OS, or Linux based PCs</p>
I normally upload it to the QGPL library. If the file suffix being uploaded is <b>.savf</b> FTP should create a valid SAVF object on the system. If it is something else, such as iquery.FILE then FTP will NOT create a valid save file on the server.
You can work around this by first creating a save file on the IBM i server using the CRTSAVF CL command.</p>
<pre>CRTSAVF QGPL/IQUERY</pre>
<p>Once uploaded, use the RSTLICPGM CL command to install SQL iQuery. However, before you do that, it is recommended that you deleted any current installation of SQL iQuery.
To check which version, if any, you currently have installed, use the LICPGM menu.</p>
<pre>GO LICPGM </pre>
<p>Next scroll down, usually to the bottom of the list, and see if 2COZ-IQ<i>n</i> is installed, where <i>n</i> is the iQuery version (normaly 6, 7 or 8). If it is installed, first remove that installation to prepare for the new version.</p>
<pre>DLTLICPGM 2COZIQn</pre>
<p>Again, where <i>n</i> is the installed version number.</p>
<p>Once deleted or if it wasn't installed, proceed with the following installation command:</p>
<pre>RSTLICPGM 2cozIQ8 *SAVF SAVF(QGPL/IQUERY)</pre>
<p>Note: Use the save file name IQUERY72 if you are running on IBM i V7R2.</p>
<p>Once complete, you are prompted for some install-time customizations. After that screen is completed, SQL iQuery is installed and ready to go.</p>
<p>We include several SQL iQuery Scripts with SQL iQuery. You can verify that everything is installed correctly by running one of these scripts. For example our <i>demo</i> script can be run by running the following CL command:</p>
<pre>RUNiQRY *DEMO</pre>
<h3>Fixes and Enhancements Log</h3>
The following are recenty enhancements and fixes to SQL iQuery
<table>
  <tr>
    <th>Released Date</th><th>Description</th>
  </tr>
  <tr><td>21-JUNE-2024</td>
    <td>Corrected an issue withe IQRYEMAIL - the SQL iQuery interface that evokes the email client selected during installation. It was not clearing a structure and 
    caused garbage characters to appear in the email when sending attachments.</td>
  </tr>
  <tr><td>10-MAY-2024</td>
  <td><p>Converted SQL iQuery to a no-charge (non-license key) product. Anyone may download, install and use SQL iQuery for free; no license key required.</p>
    <p>Support and training are chargable, if needed. Please contact Bob Cozzi for support and training options.</p></td></tr>
  <tr>
    <td >14-NOV-2023</td>
    <td><p>Corrected an issue with EMAIL options where the new FROM ADDRESS would not
              properly replace the configuration record &FA code when no address is specified.</p>
           <p>Corrected an issue where users would edit the config.xml file in the iQuery config
              folder, changing the <excel> tags and it would improperly use any value other than
              ACS as the file suffix. This has been corrected.</p>
           <p>Corrented an issue during install that would insert an improper <excel> tag
              when the iQuery option is selected during install.</p>
           <p>Enhanced the WRKFUNC (Work with SQL Functions) command. It is now a stand-alone
              interface and works on international language systems.</p>
   </td>
  </tr>
<tr>
  <td>21-SEP-2023</td><td>Corrected an issue when STMF(XXXXXXX) is specified and STMFNAME(*STMF) is also
              specified. The program would create a folder named XXXXXXX and then create
              the output streamfile on the IFS in /home/&lt;user&gt;/xxxxxxx/xxxxxxx.xls
              Now it works as expected and creates the file /home/&lt;user&gt;/xxxxxxx.xls</td>
                
</tr>
</table>
