# TemplateToPdf.Demo
This is a demo applciation for Umbraco Template to Html

# What is this package for? 
This package is desgined to convert Umbraco Cotnent into Pdf while you have a full control of what the pdf shall look like using confgration from Umbraco back office! 

# Exmaple:
Using Umbraco Starter-kit, i added a button on the buttom of each one of those cool people to download thier resumes: 
![139023905-54d7e6db-5a46-41d6-96e1-b88a75369d71-min](https://user-images.githubusercontent.com/28313687/139027898-38f9929b-8aa7-4944-85ef-b0c5bc790bcd.png)

Now! when you click on the button it will open up a pdf file took its content from UmbracoCms and the structure/style from a Template also in Umbraco!

This the template Used => 
![139024501-c26c9b75-4eeb-4b90-899a-def7ba3a783f-min](https://user-images.githubusercontent.com/28313687/139027997-260b0238-aab1-4f03-bf71-f0841e3fc873.png)
 
Now Lets see the Content : 
Here we got the details for each Person :
![139024974-08b043db-cb2e-4ae8-b259-6d799ec514ff-min](https://user-images.githubusercontent.com/28313687/139028284-f29b7186-c900-4fec-8536-79356a4dc04c.png)

Now lets check the Pdf! : 
![139025176-d4f964cb-14f0-432f-8027-17b83d201d2e-min](https://user-images.githubusercontent.com/28313687/139028356-8ea2731f-671a-41d7-9d0d-e49ee0d24c3d.png)


Now! Lets say we want to make his name on a different color and check a few lines on the objectve  
Those are our changes we saved and published them:
![139025595-3553ff95-2bc9-481a-9ed2-109e4b1e7bbf-min (1)](https://user-images.githubusercontent.com/28313687/139028413-bafbdf45-5f2c-4fe1-b997-2f5ab22e361e.png)

now to see the new pdf , All you have to do is refresh !! 
![139026247-3c7a6d9e-4a94-4fc4-aaa2-2e7ccaece65d-min](https://user-images.githubusercontent.com/28313687/139028461-97f69a0f-88f2-4593-89e7-67d13462829f.png)

This is The Pretty much the TemplateToPdf Package 


# Getting Started 

1.	2.1 First Thing First: 
      Download the package Using: 
>dotnet add package UmbracoTemplateToPdf --version 1.0.5

2.2 Adding The Core file
you need to add a file called: wkhtmltopdf.exe this file is 
responsible for converting the Html inside of the template to Pdf.
you can download it from here : 

https://github.com/uppercuut/TemplateToPdf.Demo/tree/master/TemplateToPdf.Demo/wwwroot/TemplateToPdf

Life location must be: 
“<YourApplicationName>/ wwwroot/TemplateToPdf/wkhtmltopdf.exe” 
if the folder “TemplateToPdf” is not there create one.

2.3 Configuring the Startup.cs
add this line to the startup file and you are ready to go!
 
**services.AddTemplateToPdf(_env);**
 
like the Image Bellow:
      
![image](https://user-images.githubusercontent.com/28313687/139026489-84c8afb5-368f-47b7-9c0a-7748623c44e2.png)


