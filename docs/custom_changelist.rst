===============================================
Customizing Changelist Description in Perforce!
===============================================

Customizing Default Changelist Description in Perforce
======================================================

To improve the traceability of commits to perforce, we were looking to
provide a changelist description template to the team. We use Perforce
as a repository running on a Windows platform.

Research from the internet suggested that we would have to use P4
triggers. However, our IT team had restricted the usage of triggers on
our perforce server. So, my colleague, Krishna (https://krishkasula.github.io/
), ended up writing a client-side python script
that allowed us to customize the changelist description for Perforce.

Script:

.. code:: python


   #! /usr/bin/env python3
   # ------------------------------------------------
   # Author:    krishna
   # Created:   Wed Jun 12 11:26:39 2019 IST
   # USAGE:
   #       createNewChange.py
   # Description:
   #   Creates a new numbered perforce change and shows the Number in a dialogue box
   #
   # ------------------------------------------------
   import ctypes
   from P4 import P4

   def main():
       '''The Main'''

       # Create a new perforce object and connect
       p4obj = P4()
       p4obj.client = 'user_workspace'
       p4obj.connect()
       if not p4obj.connected():
           ctypes.windll.user32.MessageBoxW(0, "Unable to Connect", "Error", 0)
           return

       # Create a new perforce change with below description
       change = p4obj.fetch_change()
       change._description = """
       Fix for STAR:
       Release (LCA/GA/version):
       Customer Name?
       For RCT?
       Section that is changed in the source:
       Creating PDF?
       PDF Edition Number?
       Technical Review Done?
       G.Review?
       Related HLA:
       """

       # Save and show it on a dialogue box
       ctypes.windll.user32.MessageBoxW(0, *p4obj.save_change(change), "New P4 Change", 0)

       p4obj.disconnect()


   if __name__ == '__main__':
       main()

Prerequisites for Running the Script
------------------------------------

1. Install Python 3. Ensure that you let the installer to update the
   environment variables.
2. Install p4python. Use the following command:
   ``pip3 install p4python``

How the Custom/Personalzied Changelist Script Works
---------------------------------------------------

1. Run the script:

   1. Save the script to your computer with the .py extension. For
      example, I saved the script to the file: ``create_changelist.py``.
   2. Update the string ``user_workspace`` with your P4 workspace.
   3. To customize the changelist description, edit the text in the
      block: ``change._description = """    .....   """``
   4. Double-click the python file (``create_changelist.py``) to execute
      it.

   A new numbered changelist (each changelist other than the *default*
   changelist has a number) is created. If successful, you must see a
   message similar to the following:

   .. figure:: ./successful_command.png
      :alt: Numbered Changelist is created

      Numbered Changelist is created

2. When you open the Perforce client (we use Perforce Helix P4V) and try
   to check out a file/folder, the changelist created in Step 1 is
   available in the dropdown.
3. Select the changelist. The changelist is auto-populated with the
   template description.
4. Fill the description and continue the check out.
