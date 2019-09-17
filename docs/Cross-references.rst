==========================================================================
Retain Formatting After Updating a Cross Reference
==========================================================================

Problem
~~~~~~~

You insert a cross reference to a section. And, you apply a character style to display the link in blue. However, when you update the cross reference, the character styling is lost. For example, if you have applied a style to display the link in blue, the formatting is lost when you update the cross reference. The link does not appear in blue anymore.

Tool: Microsoft Word

Workaround
~~~~~~~~~~

To retain the character styling of a cross reference after updating it, do the following:

1. Right-click the cross reference, and select **Toggle Field Code**.
    
   The field code is displayed. The field code is similar to the following:

   ``{REF _Ref485728411 \h}``

2. Append the following string to the field code:

   ``\*Charformat``    
   
   So, the cross reference field code must be similar to the following:
   
   ``{REF _Ref485728411 \*Charformat \h}``
   
3. Right-click the cross reference, and select **Toggle Field Code**.

4. Select the cross reference and apply the character style that you want to use. For example, apply blue font color to the cross reference.

5. To test the solution, right-click the cross reference and select **Update Field**. The blue color must be retained after the update.


