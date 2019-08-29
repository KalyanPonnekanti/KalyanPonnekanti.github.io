Using IPXACT to Generate Documentation
======================================

Since last year, we have seen an increasing interest from customers
regarding IPXACT. Customers specifically request the external interfaces
and register descriptions in the IPXACT. Recently, we had a customer who
requested DITA sources as well as IPXACT. We gave early access to our
DITA sources to our customers. The initial feedback on the DITA sources
was disappointing. The customer wanted modifications to our register
layout description to match her output. This request put us in a
quandary. This customer-specific change will impact all customer
documentation. And, it would also require additional verification
effort. To resolve this issue, we scheduled a call with the customer to
understand their justification for this change. The outcome of this call
is the following use case.

Use Case: Using IPXACT to Generate Documentation
------------------------------------------------

Actor: Integration Engineer/Automation

Industry: Semiconductor

Use Case Overview: Generate external interfaces and register
documentation from IPXACT.

Basic Flow

1. Vendor provides external interface and register information in IPXACT
   format.

2. Integration engineer integrates the IPXACT into their documentation
   flow.

3. The documentation generation flow generates DITA from IPXACT.

4. The documentation publishing flow generates PDFs/HTML from DITA.

What is IPXACT?
---------------

“\ **IP-XACT** is
an \ `XML <https://en.wikipedia.org/wiki/XML>`__ format that defines and
describes individual, re-usable \ `electronic circuit
designs <https://en.wikipedia.org/wiki/Circuit_design>`__ (individual
pieces of intellectual property, or IPs) to facilitate their use in
creating \ `integrated
circuits <https://en.wikipedia.org/wiki/Integrated_circuits>`__ (i.e. *microchips*).
IP-XACT was created by the \ `SPIRIT
Consortium <https://en.wikipedia.org/wiki/SPIRIT_Consortium>`__ as a
standard to enable automated configuration and integration through
tools.”

https://en.wikipedia.org/wiki/IP-XACT

What is DITA?
-------------

“The \ **Darwin Information Typing Architecture** or **Document
Information Typing Architecture** (**DITA**) is
an \ `XML <https://en.wikipedia.org/wiki/XML>`__ `data
model <https://en.wikipedia.org/wiki/Data_model>`__ for `authoring <https://en.wikipedia.org/wiki/Authoring_system>`__ and `publishing <https://en.wikipedia.org/wiki/Publishing>`__.
It is an open
standard\ `[1] <https://en.wikipedia.org/wiki/Darwin_Information_Typing_Architecture#cite_note-dita1.2-1>`__ that
is defined and maintained by
the \ `OASIS <https://en.wikipedia.org/wiki/OASIS_(organization)>`__ DITA
Technical Committee.”

https://en.wikipedia.org/wiki/Darwin_Information_Typing_Architecture

How did We Resolve the Customer Request
---------------------------------------

As the customer requested IPXACT and DITA. We managed to convince the
customer to generate the register descriptions from the IPXACT than
reuse our DITA. However, this meant, that we had to restructure the
document (containing register information) to consolidate the register
descriptions in one Part so that customer could easily replace it with
the output from IPXACT.
