# ACTS 3: Own Your APIs, Even More So Than the Implementation
The previous chapters outlined the overwhelming need for adaptability in complex, heterogenous software systems. 
Interfaces are an essential element of managing the creation, destruction, and modification that are parts of this 
adaptability. They are the connections between the elements of capability, and especially between executable code often 
running in distinct environments. In the software-first model, application programming interfaces (APIs) become the 
foundation on which everything else is built.

Because interfaces feature so prominently, it is important to understand the tools available to an acquisition 
professional. The term software appears in the Federal Acquisition Regulation (FAR) 570 times. Upon closer inspection, 
virtually every occurrence of the term is phrased like this: “computer software and computer software documentation.” 
Further exploration reveals that the acronym API occurs across the FAR and Defense Federal Acquisition Regulation 
Supplement (DFARS) a grand total of four times. Strictly speaking, neither the FAR nor the DFARS defines regulations 
that preclude PEOs from establishing APIs as the nucleus of every weapon system acquisition. APIs live in the 
whitespaces of the regulatory landscape.

However, Section 804 of the FY21 NDAA recognized the central role of interfaces in development, giving PEOs statutory 
authority to both focus on APIs and ensure that they are discoverable via machine-readable definitions. Indeed section 
804(a)(2)(B) calls for the collection of interfaces, namely the following:

1. software-defined interface syntax and properties, specifically governing how values are validly passed and received between major subsystems and components, in machine-readable format;
2. a machine-readable definition of the relationship between the delivered interface and existing common standards or
   interfaces available in the interface repositories established pursuant to subsection (c); and
3. documentation with functional descriptions of software-defined interfaces, conveying semantic meaning of interface elements, such as the function of a given interface field.<sup>61</sup>

The law further mandates that these requirements “shall apply to any program office responsible for the prototyping, 
acquisition, or sustainment of a new or existing weapon system.” This is a powerful tool to assert control over 
acquisition destiny.
   
The DoD cannot afford to underinvest in API design. The intellectual property rights to the left or right of an API are 
negotiable, but the DoD has to control, inventory, and publish the APIs, which has to therefore come with no less than 
government purpose rights (GPR). If a program owns the API and has GPR to invoke the API as often as they like, then the 
program’s data is accessible without requiring the prime to deliver data via CD-ROMs using first-class postal service 
delivery with additional cost and unacceptable latency.
   
Let’s explore this point further. Design patterns have existed for over three decades now, and schools train every 
software architect to program to an interface, not an implementation. If the program wants record-level data access, 
define an API that supports query access to a single record. If the program wants set-level data access, define an API 
that returns a record set. If the program wants access to the entire data set, define an API that supports downloading 
a compressed file of all data in a canonized format like JavaScript Object Notation (JSON). Proper API design and 
negotiation of invocation rights at the API level mitigate the risk involved when the DoD does not own an implementation.

When the DoD owns the API, a program office can rapidly swap out a physical implementation for a virtual or game 
simulation implementation. When the program office can do so properly, it’s as easy as updating an environment variable, 
configuration flag, or feature flag. This also means the DoD cannot accept anything less than GPR on the public 
interfaces that matter, but what is on either side of that interface could be proprietary or locked down with more 
restricted rights. Thankfully, the FY21 NDAA reinforced this rights position statutorily and allowed the ability to 
retroactively assert interface rights in updated 10 CFR 2320, which now states that “the United States may release 
technical data...pertaining to an interface” for purposes of integration.

The focus on the API means the DoD needs to force the PEO to evaluate and identify system boundaries and modularity at 
the start of a new program’s journey. Interface design cannot be an afterthought; it is the forethought that determines 
the program’s ability to act as a force multiplier for programs that leaders have not even yet envisioned. However, the 
government does not need to use every internal API (and thus does not require GPR for source code), and therein lies the 
importance of system boundaries and a comprehensive understanding of separation of concerns between disparate software 
components. As an example, the need to control the API for managing the process of sending a document to a printer is 
unlikely to be as relevant as controlling the API that provides advanced searching, filtering, and querying across a 
highly relevant program data set.

On teams responding to the RFP, software engineers are likely to reply with a head shake and an eye roll when an RFP 
demands that “all software APIs must be delivered with GPR.” Instead, invest the time to identify the system boundaries, 
understand where the program benefits from establishing a separation of concerns via APIs, and demand unlimited rights 
or GPR on those things only. This is an exercise in intelligence that only the program, not the contractor, can perform. 
In our vignette that illustrates all of these ACTS in a more concrete fashion, we will explicitly demonstrate this 
concept for additional clarity.

An API is not a Word or PDF document describing a data exchange. Begin to view an API as an interactive boundary that
establishes a separation of concern between critical system modules. The API manifests its power only when it is 
physically exercised and made available in a machine-readable format. However, this a dangerous area because PEOs and 
program managers have to discern the nuances of different types of APIs and understand how to define, document, and 
publish them. The highly popular OpenAPI is wonderful for representational state transfer (REST) software 
architectures.<sup>62</sup> However, this standard is at best incapable and at worst wholly inapplicable for describing 
service-oriented architectures, interfaces for working field programmable gate arrays (FPGAs), or graphics processing 
units (GPUs, e.g., CUDA®, a parallel computing platform and programming model developed by NVIDIA), among others. RFPs 
cannot adequately capture the APIs of a system-of-systems merely by mandating documentation of all interfaces using 
OpenAPI.

> Progressive PEOs have the ability to reuse and expand on existing guidance to create their own code inventory across 
> all of their programs. Consider leveraging the existing DOD consensus standard metadata schema as your starting 
> point.<sup>63</sup> Our recommendation is to add a single new stanza that contains a uniform resource name (URN) 
> identifying a set of APIs, an enumeration that captures the type of API (e.g., REST, SOAP, CORBA, GRAPHQL, etc.), 
> and two uniform resource locators (URLs) that point to the human-readable and machine-readable documentation 
> respectively.

Additionally, ensure you use cloud-native principles to build the system in which these APIs operate. Contrary to 
popular belief, a cloud-native architecture actually has little to do with the cloud; more accurately, it captures how 
an application relies on horizontal scaling to elastically respond to spikes in demand. If vertical scaling software is 
about adding more memory and more CPUs to a single machine, horizontal scaling and cloud native architectures implement 
elasticity by adding more low-cost machines horizontally. The DoD has already established through a very public 
demonstration in 2020 that it can deploy cloud-native in embedded systems just as easily it can in a hyperscaler cloud 
service provider ecosystem.<sup>64</sup>

## Corollary: Ensure the APIs Provide Access to All the Data the Program Cares About
Carefully consider future program data aspirations and design APIs that account for not only the primary data sets but 
the tributaries that flow underneath the surface of the application. Many DoD programs failed to recognize the inherent 
value of an application’s data streams and, under the guise of a vendor’s “intellectual property” stamp, lost access to 
their own data.

We intentionally use the plural streams in this corollary, and it’s worth further explanation using a water analogy. 
The Mississippi River comprises flows from the Arkansas, Illinois, Missouri, Ohio, and Red Rivers. The Tennessee, 
Allegheny, Scioto, and other rivers feed the Ohio River. When you visit the Mississippi River Delta, it’s easy to 
inadvertently forget about the headwaters and tributaries. If the US suddenly sold the water rights for each of the 
tributaries, what value would there be in owning the rights to the waters in the Mississippi itself?

By extension, it is easy to focus on the major application data sets, analogous to the mighty Mississippi. There are 
other headwaters and tributaries that PEOs cannot overlook, including software supply chain data in the form of an SBOM 
and highly relevant cyber resiliency data sets produced within the CI/CD pipeline, especially the pipelines measurement 
for mean time to recovery (MTTR), runtime telemetry data that represents how users navigate and interact with the 
software, and other examples.

PEOs can find greater value and resiliency by pivoting away from defining specific data sets that must be delivered via 
CD-ROM media and instead focus on an adaptable set of APIs that contracts obligate implementers to implement. Rigid data 
set definitions could preclude innovation and growth, whereas a well-defined API accessible with GPR not only ensures 
data accessibility for data science activities but also serves as a proven mitigation strategy against the dreaded 
proprietary data claims of a defense contractor.

If PEOs can employ APIs to intrinsically assure the government data rights it needs, that does not mean the data will 
be easily accessible. The final step is to ensure a robust set of APIs that have the capability to fetch a singular 
record set, sorting and filtering capabilities to reduce noise when seeking a reduced data set across the complete data 
catalog, robust pagination capabilities to avoid asking for a 2-TB data set in a single request, and perhaps the ability 
to make long-running data requests where the system assembles data over minutes or hours and makes a programmatic 
callback to inform the system making the request that the data set is now available for download at this location.
