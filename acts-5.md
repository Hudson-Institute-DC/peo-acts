# ACTS 5: Think in Service Levels
Accountants think in terms of spreadsheets, graphic artists in terms of visual images, and project managers in terms of 
the venerable Gantt chart. The Gantt chart is excellent for assembling a list of tasks, dependencies, and milestones and 
visualizing progress to date. This project management tool has proven indispensable for coordinating industrial 
activities across a production floor at a given time—conduct physical activities to ensure a resource is available at 
this location not later than this milestone. In the industrial setting, the hard part is not connecting the pieces, it 
is getting all the pieces to arrive on the factory floor at just the right moment.

The very essence of software, and in particular DevOps, is the opposite. Generally speaking, highly advanced commercial 
software is available on demand for access, from state-ofthe-art enterprise resource planning (ERP) to product life 
cycle management (PLM) software and from learning management systems (LMS) to human resource management systems (HRMS). 
The hard part is not getting all the pieces to arrive by a milestone with software, it is connecting them to 
interoperate reliably and at speed. The data integration market is growing at a compound annual growth rate (CAGR) of 
nearly 12 percent, and experts expect it to achieve a market share in excess of $19 billion within the next four 
years.<sup>69</sup>

Software development tools, programming languages, codified design patterns, and the advent of programming with Google 
(in which a developer uses Google to find a snippet of code that meets their immediate needs) have made software 
development easier than it historically has been. It is the integration between different architectures and API styles 
and dozens of identical programming standards (as depicted in an infamous XKCD cartoon<sup>70</sup>) that creates 
delivery delays and affects the reliability and operational speed of a system. Software integrations are not analogous 
to twentieth-century industrial integrations, and the Gantt chart has proven to be an unreliable management technique 
for software integration activities.

We can simplify software integration to the concept that data is in motion. Data in motion is transiting across 
distinct and easily identifiable system boundaries. It should be obvious that modern standards judge any system that is 
unreliable or unavailable as a failure. As reliability and speed demands on the data in motion increase, so too does 
the operational cost.

Organizations measure and capture reliability and speed using service levels. For example, Google defines precise 
numerical targets for system availability using a service level objective (SLO), enabling developers to frame design 
or architectural discussions around quantitative targets that they must meet or exceed.<sup>71</sup> Where the SLO is 
developer-centric, the service level agreement (SLA) is typically a legal instrument that establishes thresholds and 
penalties, typically financial penalties, when systems do not meet performance targets. Logically, the SLA might 
establish a set of metrics that must be at least 99.9 percent, while internally the development team might be operating 
against a SLO that defines the same set of metrics at 99.95 percent. Finally, the service level indicator (SLI) is the 
discrete measurement of successful probes against the set of metrics the team uses to calculate the actual service 
availability percentage.

If it is possible to cleanly express both reliability and speed and if established vendors can demonstrate SLIs that 
meet or exceed those metrics, the PEO’s first instinct should be to outsource that capability to a commercial or dual-
use provider. The PEO should focus on building novel solutions for the undefined requirements that cannot readily define 
reliability and speed or that a provider cannot demonstrably meet. When the act of production is difficult, PEOs should 
want diamonds, and when the speed and reliability of data in motion are difficult, they should want service levels.

## Corollary: The Lollipop is More Important Than the Enterprise Architecture
The DoD operates an exceptional logistics network capable of moving people and materials around the planet at 
extraordinary speeds. It is possible to easily define an SLA for routine envelope, package, and pallet delivery to any 
US military base around the world. Outsource that. Is it possible to define an SLA for the insertion of special forces 
in an austere environment while under hostile fire? No. There are too many variables, yet this is precisely the type of 
activity that the DoD must accomplish with precision and reliability. The government, and in particular the DoD, 
explicitly owns force generation.

Purists will argue the only thing that matters is the enterprise architecture (EA): if the program gets the EA right, 
everything else will just work. We argue that this is a naive position because the modern world is built from 
systems-of-systems, and it is the integration between disparate software systems that drives economies and creates 
disproportionate battlefield advantage against peer competitors.

There is value in adopting enterprise architecture activities within a program, but PEOs and program managers need to 
accept the inherent brittleness when hundreds, if not thousands, of discrete systems come together to achieve force 
projection downrange that realizes a kill chain. Who can identify a singular set of DoD Architecture Framework (DoDAF) 
models that capture the unified EA for the system-of-systems required to insert that special forces team?

The “lollipop” is a colloquialism that software developers use within the unified modeling language (UML) to represent 
a software interface.<sup>72</sup> Measuring the reliability and speed of data across an interface is common practice. 
How do you measure reliability and speed of data using a DoDAF model on a printed sheet of paper?

When PEOs actively think in service levels, it marginalizes the need to have difficult conversations about the right 
intellectual property posture or contract structure. It avoids believing in paper models that seemingly project 100 
percent reliability. The EA of Amazon’s, Microsoft’s, and Google’s cloud is likely very impressive, but let’s not 
forget recent headlines:

* Google Cloud Outage Takes Major Websites and Apps“ ߪ Down”<sup>73</sup>
* Extended AWS Outage Disrupts Services across the“ ߪ Globe”<sup>74</sup>
* Azure’s DNS Problem Highlights Fallibility in Cloud Ser“ ߪ vices”<sup>75</sup>

When commercial tech giants like Google, Amazon, and Microsoft cannot achieve 100 percent reliability and speed of data 
in motion, PEOs cannot accept the position that if they get the EA right, everything else will just work. Never accept 
the idea that a model is more powerful than a functioning interface and avoid the acquisition original sin of 
predilection for prediction. Focusing on the lollipop inherently drives outcome-based thinking. Software integration 
outcomes occur only through interfaces, and the PEO can measure, monitor, and, in extreme cases, rapidly pivot 
interfaces to another service provider that implements the exact same interface.