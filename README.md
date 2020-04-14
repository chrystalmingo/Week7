# Project 7 - WordPress Pentesting

Time spent: 9.5 hours spent in total

> Objective: Find, analyze, recreate, and document 5 vulnerabilities affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability: Authenticated Stored Cross-Site Scripting
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2 
    - Fixed in version: 4.3
  - [ ] GIF Walkthrough: 
  ![](XSS1.gif)
  
  - [ ] Steps to recreate: Make a new post >> Write the following javascript"<script type="text/javascript">alert("You just got Hacked!!!");</script>" Publish it >> Then view to post!
  
2. (Required) Vulnerability: Authenticated Stored Cross-Site Scripting
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version:4.2
    - Fixed in version: Later Version
  - [ ] GIF Walkthrough: 
  ![](XSS2.gif)
  - [ ] Steps to recreate: Make a new Post >> Place the text Danger ahead! Potential Hacker
   <img src="PUT IMAGE LINK HERE" onmouseover="alert('Caught you! :D')"> . You should see something and then an alert appear.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/branches/4.2/src/wp-admin/includes/image.php)
    
3. (Required) Authenticated Stored Cross-Site Scripting via Image frame
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6.1
  - [ ] GIF Walkthrough: 
   ![](XSS3.gif)
  - [ ] Steps to recreate: Upload a new image to the library >> Then click on that image >> Then in the title section, add the following JavaScript "<IMG SRC="#" ONERROR="alert('HACKED HACKED HACKED')"/>" >> Then clck next to the image name.
  
  4. (Optional) Optional)Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: This vulnerablity allows remote attackers to inject arbitrary web script or HTML via video URL in YouTube emebeds.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: Later Version
  - [ ] GIF Walkthrough: 
   ![](XSS4.gif)
  - [ ] Steps to recreate: Make a new page and paste the code below:
 
    ```
    <iframe width="560" height="315" src="https://www.youtube.com/embed/IZy6Z9_2ZHQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    
    ```
    
    5. (Optional) Vulnerability Name or ID: User Enumeration
    - [ ] Summary: This vulnerablility will remote attackers to create a crafted image file name that will inject arbitrary web script.
    - Vulnerability types: User Enumeration
    - Tested in version: 4.2
    - Fixed in version: Later Version
  - [ ] GIF Walkthrough: 
   ![](XSS5.gif)
  - [ ] Steps to recreate: Attempt to log into admin without the use of the password. after that do the same with an incorrect password , finally attempt to log in with user.
   - [x] Link to affected code: 
     [Link](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
     
    ## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2020] [Chrystal Mingo]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
