# SQLiQuery
<b>SQL iQuery</b> for IBM i *SAVF download image
Licensed Program COZ-IQ8 
A Web, CL and Interactive SQL query tool for IBM i.
It replaces the legacy Query/400 and provides an SQL/RPG style scripting langauge for more powerful queries.
With SQL iQuery you can:

<ul><li>Command Entry</li><li>HTML/Javscript Web pages</li><li>CL programs</li><li>menus</li><li>the job scheduler</li>
<li>batch jobs</li></ul>
The following are recenty enhancements and fixes to SQL iQuery
<table>
  <tr>
    <th>Released Date</th><th>Description</th>
  </tr>
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
              the output streamfile on the IFS in /home/<user>/xxxxxxx/xxxxxxx.xls
              Now it works as expected and creates the file /home/<user>/xxxxxxx.xls</td>
</tr>
</table>
