Download Link: https://assignmentchef.com/product/solved-sdev300-week8-web-forms
<br>
This exercise  uses the AWS Cloud9 environment develop and fully test a set of tools and Web Forms to perform the following functionality:

<ol>

 <li>Password Login form – This Python form allows a user to login to a simple web application with a username and password. A file can be used to store the username and password for validated users for this activity. No additional Web application functionality is needed after successful login other than a Greeting of your choice and the ability to update the password in a form.</li>

 <li>Password update Form – This Python form allows a user to update a user’s password after they have successfully logged in.</li>

 <li>Authentication functions – These Python functions that will check the following NIST SP 800-63B criteria are met upon login or upon password update:  SHALL be at least 8 characters in length

  <ul>

   <li>SHOULD be no more than 64 characters in length</li>

   <li>SHALL compare the prospective secrets against a list that contains values known to be commonly-used, expected, or compromised (Provided as CommonPasswords.txt)</li>

   <li>If the chosen secret is found in the list, the application SHALL advise the subscriber that they need to select a different secret, SHALL provide the reason for rejection, and SHALL require the subscriber to choose a different value</li>

   <li>SHALL implement a time-based rate-limiting mechanism that effectively limits the number of failed authentication attempts that can be made on the subscriber’s account. For this exercise throttling should start after 15 attempts.</li>

   <li>When the subscriber successfully authenticates, the verifier SHOULD disregard any previous failed attempts for that user from the same IP address</li>

  </ul></li>

 <li>Logger – Create a log to log all failed login attempts. The Log should include date, time and IP address.</li>

 <li>Log Analyzer – Create a Python log analyzer application that reads the log file created in part d to identify and geo-locate all IP addresses where more than 10 failed attempts in a period of less than 5 minutes. The geolocation should include the Lat/Long value provide from the IP Address location.</li>

</ol>

A sample report might look like this:

100.16.4.23 had 12 failed login attempts in a 5 minute period on Jul 7, 2019.

100.16.4.23 has a Lat/Long of 41.2908816/-73.610759.




Hints:

<ol>

 <li>Start early. This will take you longer than you think.</li>

 <li>Leverage the File I/O, Flask and Data structures work previously performed in the class.</li>

 <li>Use functions to enhance code reuse and modularity.</li>

 <li>Use the AWS Cloud9 IDE.</li>

 <li>Use Python Lists or other data structures to store the Common Passwords and then appropriate search functions to expedite comparisons.</li>

 <li>You can use “request.environ[‘REMOTE_ADDR’]” to obtain the client IP address. You will need to import the request package: “from flask import request”.</li>

 <li>You will need to load the ip2geotools Python module to perform the GeoLocation (sudo python3 -m pip install ip2geotools). You will need to import the IpCity Package (from</li>

</ol>

ip2geotools.databases.noncommercial import DbIpCity). See the ip2geotools for additional method and objects available.

<ol start="8">

 <li>Be sure to send me questions, if you need assistance.</li>

 <li>Using the Decrypting Secret Messages sites found in this week’s readings, decrypt the following messages<strong>. </strong>

  <ol>

   <li>– …. .. … / … -.. . …- / …– —– —– / -.-. .-.. .- … … / …. .- … / … — — . / … – .-. .- -. –. . / .-. . –.-</li>

  </ol></li>

</ol>

..- . … – … .-.-.-

<ol>

 <li>U28gdGhpcyBpcyBiYXNlNjQuIE5vdyBJIGtub3cu</li>

 <li>— Psuwb Ysm —-</li>

</ol>

W oa gc qzsjsf. Bc cbs qcizr dcggwpzm twuifs hvwg cih.  — Sbr Ysm —

Provide the decoded message along with the Cipher and any other parameters you used to solve each puzzle.

Hints:

<ol>

 <li>Use the rumkin site</li>

 <li>You will need to experiment some to narrow down the possible algorithms used. Some are more obvious than others.</li>

 <li>You will know when you have selected the correct Cipher</li>

</ol>

Document your results of the application running from the AWS Cloud9 classroom environment.  Provide your test results for each requirement in the Web application, associated functions and the log analyzer program. Describe the results of your NIST password complexity functions and how you tested each requirement. Include the Cipher tool results and write up in this document as well