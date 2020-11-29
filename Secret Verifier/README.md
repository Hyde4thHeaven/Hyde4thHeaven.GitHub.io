# Look-up Secret Verifier in Security Requirements based on Application Security Verification and Digital Identity Guidelines  
`29 November 2020`
<hr>  
  
## Main Goals
+ to help organizations develop and maintain secure applications.  
+ to allow security service vendors, security tools vendors, and consumers to align their requirements and offerings.  
  
## Application Security Verification Levels
> The Application Security Verification Standard defines three security verification levels, with each level increasing in depth.  
+ **Level 1 - First steps, automated, or whole of portfolio view** is for low assurance levels, and is completely penetration testable  
+ **Level 2 - Most applications** is for applications that contain sensitive data, which requires protection and is the recommended level for most apps  
+ **Level 3 - High value, high assurance, or high safety** is for the most critical applications - applications that perform high value transactions, contain sensitive medical data, or any application that requires the highest level of trust. Each ASVS level contains a list of security requirements.  
  
## Look-up Secret Verifier Requirements
> *Look up secrets* are pre-generated lists of secret codes, similar to Transaction Authorization Numbers (TAN), social media recovery codes, or a grid containing a set of random values. These are distributed securely to users. These lookup codes are used once, and once all used, the lookup secret list is discarded.  
>> This type of authenticator is considered **”something you have”.**  
  
**Secret Verifier** is suggested to only Level 2 and Level 3 applications due to its almost strong security but need complicate procedure to create the environment system. 
  
### 1. Verify that lookup secrets can be used only once.  
Verifiers of look-up secrets SHALL prompt the claimant for the next secret from their authenticator or for a specific (e.g., numbered) secret. A given secret from an authenticator SHALL be used successfully only once. If the look-up secret is derived from a grid card, each cell of the grid SHALL be used only once.  
  
### 2. Verify that lookup secrets have sufficient randomness.  
Verifiers SHALL store look-up secrets in a form that is resistant to offline attacks:  
> + [x] *Look-up secrets having at least 112 bits of entropy* SHALL be hashed with an approved one-way function.  
> + [x] *Look-up secrets with fewer than 112 bits of entropy* SHALL be salted and hashed using a suitable one-way key derivation function. The salt value SHALL be at least 32 in bits in length and arbitrarily chosen so as to minimize salt value collisions among stored hashes. Both the salt value and the resulting hash SHALL be stored for each look-up secret.
> + [x] *For look-up secrets that have less than 64 bits of entropy*, the verifier SHALL implement a rate-limiting mechanism that effectively limits the number of failed authentication attempts that can be made on the subscriber’s account.  
  
### 3. Verify that lookup secrets are resistant to offline attacks, such as predictable values.  
The verifier SHALL use approved encryption and an authenticated protected channel when requesting look-up secrets in order to provide resistance to eavesdropping and MitM attacks.  

______________________________
<table border="0">
 <tr>
   <td> <h3><i>Although my profile picture is quiet, but the real me can make some noise.</i></h3>
      <hr>
      <b><font color="Blue"> Author: Vuttawat Uyanont </font></b>  <br>
      <font color="grey"><i>Sexiest former engineer and banker who interested in IT & Tech, Sake, and Beer.</i></font>  <br>
      <b>Studying:</b> Master Computer Science in Cybersecurity Management at Mahanakorn University.  <br> </td>  
   <td><img src="https://github.com/Hyde4thHeaven/Hyde4thHeaven.GitHub.io/blob/main/How-to-Create-GitLab-Pages/img/author.png" width="150"/></td>  
 </tr>
</table>
