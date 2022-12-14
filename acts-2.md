# ACTS 2: Partner with an Authorizing Official to Realize a Continuous Authorization to Operate
The previous chapter discussed the development environment as a production environment. Operating a software factory is 
the precursor to modern software development, and the factory cannot begin operating until the system where it operates 
has received an authorization to operate (ATO). New programs need to recognize this dependency early and consciously 
build a partnership with their authorizing official (AO). Why? There are too many AOs who are simply unsure what 
“shifting cybersecurity left into the CI/CD pipeline” means, what it accomplishes, or why they should support these 
activities because they (the AOs) have not been involved in modern software development techniques or tooling (see 
MOCAS conversation in the previous chapter).

Program managers can benefit from establishing direct knowledge of the most recent DoD guidance on the realization of 
continuous ATOs (cATOs). In 2022, the DoD’s senior information security officer (SISO), David McKeown, released a 
highly relevant memo that outlines the minimum requirements for obtaining a cATO.<sup>59</sup> This memo establishes continuous 
monitoring, active cyber defenses, and a secure software supply chain as so critical that they represent the minimum 
requirements to even consider operating a system under a cATO.

In particular, and building on the salient points defined in the previous chapter, the SISO memo establishes that “a 
system must embrace the DoD Enterprise DevSecOps Strategy, aligning to an approved DevSecOps Reference Design.” The 
memo essentially codifies the relationship between ACTS 1 and ACTS 2; a program that builds out a modern software 
factory is taking the requisite steps to pursue a cATO, or, if it intends to adopt an existing software factory, the 
program could benefit from its existing cATO.

Why the emphasis on a cATO over an ATO? The value to the PEO of operating under a cATO directly relates to the ebb and 
flow of software factories outlined in ACTS 1. Even during periods when the program is not aggressively pursuing new 
feature developments, operating under the cATO provides cybersecurity resiliency beyond the traditional ATO process. It 
accomplishes this through the combination of three mandatory elements outlined in the memo. Given the dynamism of 
advanced persistent threats, zero days, and the need to patch at the speed of relevance, the cATO provides the PEO with 
the greatest possible assurance. First, the software factory will be capable of performing critical software updates in 
a time of need without waiting on paperwork or paper processes that offer marginal defenses when the Cybersecurity and 
Infrastructure Security Agency (CISA) identifies a new key exploited vulnerability (KEV) that requires risk mitigation 
through concrete actions.

Second, active cyber defense goes beyond merely defending the software’s binary runtime with, including the software 
supply, the totality of intelligence available across the operational parameters of the application itself.

## Corollary: Establish an SBOM Consumption Plan
In early September 2022, the Pentagon temporarily halted deliveries of F-35 fighters when it discovered that 
manufacturers had sourced raw materials from China to produce a magnet. The modern software supply chain is even more 
complex, and the impact and role of open-source software across the supply chain are virtually inescapable. It is 
unreasonable to expect the DoD to develop all software systems from scratch without accepting either direct or 
transitive dependencies on open-source software. The ubiquitous Linux operating system depends fully on open-source 
software libraries, and even firmware found in chips can include open-source software—all of which foreign nationals 
subject to their countries’ draconian laws might have influenced, designed, or perhaps implemented. Instead of fearing 
open source, treat it like any other program risk and make risk-informed decisions by using a proper risk frame.

For software supply chains, the focal point is the software bill of materials (SBOM). Asking for and taking possession 
of an SBOM are insufficient measures in and of themselves to mitigate any risk. First, program managers need to be 
educated and understand the criticality of direct and indirect (transitive) dependencies. Different development 
languages use different files, notations, and mechanisms to capture all dependencies. In JavaScript, there may be a 
package.json file in a root directory, while in Go a go.mod and a go.sum file are present in the root directory. Other 
languages have their own unique ways of managing dependencies.

Knowing how to interpret SBOM data is vital for proper program risk management. For example, in our experience, it is 
common to build a software application that may define two dozen direct dependencies only to have the SBOM explode to 
literally contain hundreds of indirect dependencies that show up in the SBOM. First, not every indirect (transitive) 
dependency can affect the runtime behavior of the application. Developers use some of those dependencies to establish 
and track minimum versions of libraries in use. They may also use some of those dependencies as code generators during 
the prebuild phase of the application.

In the popular Go programming language, for example, a developer may issue a go generate command that reads in database table definitions and a set of database queries and rely on a library that dynamically creates source code to map the database and those queries. The library itself is a direct dependency (you cannot prebuild the project without it), but it is not present and cannot directly affect the runtime environment beyond the code that it generated. Unfortunately, PEOs cannot dismiss these nuances and must have access to technical experts who can decipher and discern this type of information from an SBOM.

In larger applications, it is neither unreasonable nor unexpected for a software team to hand over an SBOM that contains over 1,000 libraries. Yes, one person may build and support some of those libraries in their spare time.

Yes, some of those libraries will have open common vulnerabilities and exposures glossaries (CVEs) across the full spectrum (low, medium, high, and critical). And here’s the challenging part: not even the software team that provided the SBOM will be able to fully explain how every one of those indirect (transitive) dependencies affects the software application without painstaking and time-consuming research.

A practical conclusion from this corollary is that it is useful to access DoD software supply chain threat intelligence in order to cross-reference and risk-mitigate the well-known threats. Statistical analysis can compare a codebase to that of other programs to explore, understand, and risk-mitigate one program in the PEO that uses a software library that no other program in the PEO—or, for that matter, in the military service—is using. Analysis should include a careful evaluation and risk-mitigation of the SBOM’s outliers using the data in the SBOM to generate an open-source software nutrition label.60

We intend for ACTS 2 and this corollary to ensure that a PEO is making risk-based decisions and avoiding application of meaningless heuristics like equating the number of active contributors to an open-source library to a level of supply chain security. With one contributor or a thousand, the risks are the same, and popularity of software libraries, statistical analysis, and an effective CI/CD pipeline that reduces the mean time to recovery (MTTR) metric to minutes instead of hours or weeks will provide a high degree of cyber resiliency that both the PEO and the AO can rely upon.