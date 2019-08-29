==========================================================================
Unexpected or Corrupt Characters in Headings in a PDF Generated from Word
==========================================================================

Problem
~~~~~~~

When you convert a Word document to PDF, Heading 1 displays unexpected characters. Interestingly enough, the PDF Bookmarks do not display these unexpected characters. Following are some of the symptons:

* Text appears to melt or characters overlap
* Text includes seemingly garbage characters


Yesterday, we had a product release. We received some last minute changes to the Word source. After processing the new content, we published the Word document to PDF. Then, things started going wrong.
The chapter headings in the PDF had corrupt characters. They looked like the following:

.. figure:: ./corrupt_characters.png
      :alt: Corrupt characters in Headings

      Corrupt or Unexpected Characters in Headings in PDF

Workaround
~~~~~~~~~~

The first thing we did was to check the Word source. The Headings looked proper in the source.
We felt the encoding went wrong when converting to a PDF. So, we copied the corrupt characters and pasted them in the browser. Lo, and behold, the text was rendered properly and it matched the Word source.
Now, we were stumped on how to resolve the issue. We realized this is a recurring issue in Word sources that are edited by multiple authors (with Word language settings set to any of the European languages).
Finally, we figured the following workarounds to this issue:

* Save the document as ``.doc`` instead of ``.docx``, and publish to PDF.
* Change the font of the headings from **Helvetica** to **Arial**. 
