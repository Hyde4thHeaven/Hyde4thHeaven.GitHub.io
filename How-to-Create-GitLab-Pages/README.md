# How to create a new GitLab pages from scratch (HTML pages)

`On GitLab:`
## 1. Create a new blank project.  
<img src="./img/1.png" width="650">  
  
## 2. Detailed project.  
> **2.1** Your project name will be the path of your pages name like: https://'YourGitLabName'.gitlab.io/'YourProjectName'/  
> **2.2** Choose Visibility Level to Public, then click 'Create project' button.  
<img src="./img/2.png" width="650">  
  
## 3. Go to your project 'YourProjectName'.  

## 4. Click "+ New File" button to create a html file.  
<img src="./img/4.png" width="650">  
  
## 5. Create a html file named 'index.html' with any code you want to show your profile, then Commit changes.  
<img src="./img/5.png" width="650">  
    
## 6. Click "+ Set up CI/CD" button.  
<img src="./img/6.png" width="650">  
  
## 7. Create the master/.gitlab-ci.yml file to run your pages.
> **7.1** Create New File >> master/.gitlab-ci.yml  
> **7.2** Copy these text to the file:  
>> image: ruby:2.7  
>>  
>> pages:  
>>   stage: deploy  
>>   script:  
>>     - mkdir .public  
>>     - cp -r * .public  
>>     - mv .public public  
>>   artifacts:  
>>     paths:  
>>       - public  
>>   only:  
>>     - master  
> **7.3** Commit changes to finish.  
<img src="./img/7.png" width="650">  
  
## 8. Check Pipelines.  
> **8.1** Click shortcut CI/CD button on the left of the screen (Rocket icon).  
> **8.2** Select 'Pipelines'  
<img src="./img/8.png" width="650">  
  
## 9. Waiting until Stages of 'Update .gitlab-ci.yml' turn to green correct mark.  
<img src="./img/9.png" width="650">  
  
## 10. Finished! Enjoy your profile pages at https://'YourGitLabName'.gitlab.io/'YourProjectName'/.  
### [This is my GitLab pages, https://hyde4thheaven.gitlab.io/profile/, created by this method. Take a tour!](https://hyde4thheaven.gitlab.io/profile/)
  
______________________________
<table border="0">
 <tr>
    <td> <h3><i>"5 Easy Steps to Spot a Procrastinator:  <br>
      1. Look at</i>
      </h3>
      <hr>
      <b><font color="Blue"> Author: Vuttawat Uyanont </font></b>  <br>
      Sexiest former engineer and banker who interested in IT & Tech, and Beer.  <br>
      <b>Studying:</b> Master Computer Science in Cybersecurity Management at Mahanakorn University.  <br> </td>  
   <td><img src="./img/author.png" width="150"/></td>  
 </tr>
</table>
