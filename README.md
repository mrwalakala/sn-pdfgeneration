# sn-pdfgeneration
Link to description:
https://blog.kofko.xyz/pdf-generation-server-side
There are many ways to generate PDFs via the server side but only recently did I discover the possibility of being able to populate an existing PDF template. This can be useful in the case of graphically complex PDFs to be generated entirely in ServiceNow.

The JavaScript class to be used is PDFGenerationAPI. In particular, the fillDocumentFields method allows a filled version of a PDF to be saved on a record.

Around this method I have created this simple scope application that allows you to:

Define a PDF template per table
Using a dynamic mapping between PDF fields and fields on the table
Create the filled PDF file via UI Action on Workspace/NextExperience/UI16
After the installation you’ll find:

PDF Template table, with one demo data related for incident
UI Action “Generate PDF from template” on incident table
To use it on new table you need to define a new record on PDF Template, upload the PDF template on the new record and create a new UI Action, like the existing one on incident table.
