# TemplateToPdf.Demo
This is a demo applciation for Umbraco Template to Pdf

Backoffice Log in :

Username :admin@demo.com
PassWord: Admin12345

# What is this package for? 
This package is desgined to convert Umbraco Content into a Pdf while you have full control of what the pdf will look like using the Umbraco back office! 

# Getting Started 

1.	2.1 First Thing First: 

      Download the package using: 
>dotnet add package Our.Umbraco.TemplateToPdf

2.2 Add The Core file:

You need to add a file called: **wkhtmltopdf.exe**. This file is 
responsible for converting the Html inside of the template to Pdf.
You can download it here : 

https://github.com/uppercuut/TemplateToPdf.Demo/tree/master/TemplateToPdf.Demo/wwwroot/TemplateToPdf

The live folder location must be:

**“<YourApplicationName>/wwwroot/TemplateToPdf/wkhtmltopdf.exe” **
if the folder “TemplateToPdf” is not there then create it.

2.3 Configuring Startup.cs:

Add this line to the startup file and you are ready to go!
 
**services.AddTemplateToPdf(_env);**
 
like the image below:
      
![image](https://user-images.githubusercontent.com/28313687/139026489-84c8afb5-368f-47b7-9c0a-7748623c44e2.png)

      
# Usage 

This package is so simple to use. All you have to do is create a Url and let the browser redirect to it. 
You can use a builder from the Package that will help you a lot: 

   var pdfUrl = new PdfUrlBuilder().UsingGetByIdMethod(<yourNodeId>).WithTemplateAlias("<yourTemplateAlias>").AddPdfFileName("<pdf file name>").Url();
                  this line will generate a url to be imbeded in any page or any where ! 
      
![Untitled2](https://user-images.githubusercontent.com/28313687/139031016-9f48550f-ed5c-43b4-999f-0a80c312cbb4.png)

And this is what the Template looks like : 

![Untitled](https://user-images.githubusercontent.com/28313687/139030544-ae4e468a-791e-4321-b6cb-29ece553e0c4.png)

and @model IPublishedContent to bind the page to a loose model 

Thats it!


# Example:

Let me give an exmaple of how this package works and one of its uses! (we will walk through a scenario from A to Z)
      
Using Umbraco Starter-kit, I added a button to the bottom of each one of those cool people to download thier resumes: 
![139023905-54d7e6db-5a46-41d6-96e1-b88a75369d71-min](https://user-images.githubusercontent.com/28313687/139027898-38f9929b-8aa7-4944-85ef-b0c5bc790bcd.png)

Now! When you click on the button it will open up a pdf file, take its content from UmbracoCms and the structure/style from a Template also in Umbraco!

This is the template used => 
![139024501-c26c9b75-4eeb-4b90-899a-def7ba3a783f-min](https://user-images.githubusercontent.com/28313687/139027997-260b0238-aab1-4f03-bf71-f0841e3fc873.png)
 
Now let's see the content : 
Here we see the details for each Person :
![139024974-08b043db-cb2e-4ae8-b259-6d799ec514ff-min](https://user-images.githubusercontent.com/28313687/139028284-f29b7186-c900-4fec-8536-79356a4dc04c.png)

Now let's check the Pdf! : 
![139025176-d4f964cb-14f0-432f-8027-17b83d201d2e-min](https://user-images.githubusercontent.com/28313687/139028356-8ea2731f-671a-41d7-9d0d-e49ee0d24c3d.png)


Now! Let's say we want to make his name a different color and change a few lines of the Objective text  
Those are our changes, we saved and published them:
![139025595-3553ff95-2bc9-481a-9ed2-109e4b1e7bbf-min (1)](https://user-images.githubusercontent.com/28313687/139028413-bafbdf45-5f2c-4fe1-b997-2f5ab22e361e.png)

Now to see the new pdf. All you have to do is refresh !! 
![139026247-3c7a6d9e-4a94-4fc4-aaa2-2e7ccaece65d-min](https://user-images.githubusercontent.com/28313687/139028461-97f69a0f-88f2-4593-89e7-67d13462829f.png)

This is pretty much the TemplateToPdf Package.




