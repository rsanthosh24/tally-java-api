Tally.ERP 9 follows the XML interface for exchanging data with other systems or with other Tally.ERP 9 instances.

This XML interface specifies the following format for communication.

```
<ENVELOPE>
   
   <HEADER> . . . </HEADER>
   
   <BODY> . . . </BODY>

</ENVELOPE>
```
All kinds of interaction as in Request, Response and Error will have the same structure of xml.

---

**Header Information**

Header Tag in request contains mainly four elements:

**1. Version**

**2. TallyRequest**

**3. Type**

**4. ID**

In case of Request, header information includes mainly four elements which are Version, TallyRequest,
Type and ID. Version gives the version of the message format. Second element TallyRequest
will identify the type of request as Import or Export in the messaging format. If the value of
Tally Request is Import then the type of information would be Data, and the request will be identified
by the report name specified in ID. If the value of Tally Request is Export then the type of
information would be Data, Collection, Object or Function. The ID specifies the name of Report,
Collection, Object or function.
In the case of Response, there are mainly two elements which are Version and Status. Version
gives the version of the message format. Status indicates whether the request is success or
failure.

---

**Body Information**

This is further divided in two parts

**1. Description**

**2. Data**

Description section is used to give the description for message, request or response. Description
element mainly includes all types of variable information, storage information, computational information
and user defined TDLs. All the description information is enclosed with `<DESC>` tags.
Data section includes all the data information being transferred. All the data should be enclosed
within the `<DATA>` tags.