## How to convert pdf to text with pdf extractor sdk in Visual Basic 6 using ByteScout Premium Suite

### This code in Visual Basic 6 shows how to convert pdf to text with pdf extractor sdk with this how to tutorial

An easy to understand sample source code to learn how to convert pdf to text with pdf extractor sdk in Visual Basic 6 ByteScout Premium Suite can convert pdf to text with pdf extractor sdk. It can be applied from Visual Basic 6. ByteScout Premium Suite is the bundle that includes twelve SDK products from ByteScout including tools and components for PDF, barcodes, spreadsheets, screen video recording.

The SDK samples given below describe how to quickly make your application do convert pdf to text with pdf extractor sdk in Visual Basic 6 with the help of ByteScout Premium Suite. IF you want to implement the functionality, just copy and paste this code for Visual Basic 6 below into your code editor with your app, compile and run your application. Complete and detailed tutorials and documentation are available along with installed ByteScout Premium Suite if you'd like to learn more about the topic and the details of the API.

You can download free trial version of ByteScout Premium Suite from our website to see and try many others source code samples for Visual Basic 6.

## REQUEST FREE TECH SUPPORT

[Click here to get in touch](https://bytescout.zendesk.com/hc/en-us/requests/new?subject=ByteScout%20Premium%20Suite%20Question)

or just send email to [support@bytescout.com](mailto:support@bytescout.com?subject=ByteScout%20Premium%20Suite%20Question) 

## ON-PREMISE OFFLINE SDK 

[Get Your 60 Day Free Trial](https://bytescout.com/download/web-installer?utm_source=github-readme)
[Explore SDK Docs](https://bytescout.com/documentation/index.html?utm_source=github-readme)
[Sign Up For Online Training](https://academy.bytescout.com/)


## ON-DEMAND REST WEB API

[Get your API key](https://pdf.co/documentation/api?utm_source=github-readme)
[Explore Web API Documentation](https://pdf.co/documentation/api?utm_source=github-readme)
[Explore Web API Samples](https://github.com/bytescout/ByteScout-SDK-SourceCode/tree/master/PDF.co%20Web%20API)

## VIDEO REVIEW

[https://www.youtube.com/watch?v=NEwNs2b9YN8](https://www.youtube.com/watch?v=NEwNs2b9YN8)




<!-- code block begin -->

##### ****Form1.frm:**
    
```
VERSION 5.00
Begin VB.Form Form1 
   Caption         =   "PDF to Text"
   ClientHeight    =   1095
   ClientLeft      =   120
   ClientTop       =   465
   ClientWidth     =   3675
   LinkTopic       =   "Form1"
   ScaleHeight     =   1095
   ScaleWidth      =   3675
   StartUpPosition =   3  'Windows Default
   Begin VB.CommandButton cmd_pdf_to_text 
      Caption         =   "Convert PDF to Text"
      Height          =   855
      Left            =   120
      TabIndex        =   0
      Top             =   120
      Width           =   3495
   End
End
Attribute VB_Name = "Form1"
Attribute VB_GlobalNameSpace = False
Attribute VB_Creatable = False
Attribute VB_PredeclaredId = True
Attribute VB_Exposed = False
Private Sub cmd_pdf_to_text_Click()
    
    ' Hanlde Error
    On Error GoTo ErrorHandler:
    
    ' Create Bytescout.PDFExtractor.TextExtractor object
    Set extractor = CreateObject("Bytescout.PDFExtractor.TextExtractor")
    
    ' Set Registration name and key
    extractor.RegistrationName = "demo"
    extractor.RegistrationKey = "demo"
  
    ' Load sample PDF document
    extractor.LoadDocumentFromFile "sample.pdf"
    
    ' Peform Save to Text file
    extractor.SaveTextToFile "output.txt"
    
    ' Show Success Message
    MsgBox "Extracted data saved to 'output.text' file.", vbInformation, "Success"
    
    ' Close form
    Unload Me
    
ErrorHandler:
If Err.Number <> 0 Then
    MsgBox Err.Description, vbInformation, "Error"
End If

End Sub

```

<!-- code block end -->    

<!-- code block begin -->

##### ****PDF_To_Text.vbp:**
    
```
Type=Exe
Reference=*\G{00020430-0000-0000-C000-000000000046}#2.0#0#..\..\..\..\..\..\..\..\..\Windows\SysWOW64\stdole2.tlb#OLE Automation
Reference=*\G{F1D62CEE-68AA-4F38-9DB0-8021C13255D8}#9.1#0#..\..\..\..\..\..\..\..\..\WINDOWS\SYSWOW64\Bytescout.PDFRenderer.tlb#ByteScout PDF Renderer SDK [TRIAL]
Form=Form1.frm
Startup="Form1"
Command32=""
Name="PDFToText"
HelpContextID="0"
CompatibleMode="0"
MajorVer=1
MinorVer=0
RevisionVer=0
AutoIncrementVer=0
ServerSupportFiles=0
VersionCompanyName="Hiren"
CompilationType=0
OptimizationType=0
FavorPentiumPro(tm)=0
CodeViewDebugInfo=0
NoAliasing=0
BoundsCheck=0
OverflowCheck=0
FlPointCheck=0
FDIVCheck=0
UnroundedFP=0
StartMode=0
Unattended=0
Retained=0
ThreadPerObject=0
MaxNumberOfThreads=1

```

<!-- code block end -->