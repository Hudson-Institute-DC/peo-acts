# Executive Summary

You would not be reading this if you did not realize that it is important for the Department of Defense (DoD) to get 
software right. There are two sides to the coin of ubiquitous software for military systems. On one side lies untold 
headaches—new cyber vulnerabilities in our weapons and supporting systems, long development delays and cost overruns, 
endless upgrade requirements for software libraries and underlying infrastructure, challenges in modernizing legacy 
systems, and unexpected and undesirable bugs that emerge even after successful operational testing and evaluation. On 
the other side lies a vast potential for future capability, with surprising new military capabilities deployed to 
aircraft during and between sorties, seamless collaboration between military systems from different services and 
domains, and rich data exchange between allies and partners in pursuit of military goals. This report offers advice to 
help maximize the benefits and minimize the liabilities of the software-based aspects of acquisition, largely through 
structuring acquisition to enable rapid changes across diverse software forms.


This report features a narrower focus and more technical depth than typical policy analysis. We believe this detail is 
necessary to achieve our objectives and reach our target audience. We intend this to be a useful handbook for the DoD 
acquisition community and, in particular, the program executive officers (PEOs)<sup>1</sup> and program managers as they 
navigate a complex landscape under great pressure to deliver capability in an environment of strategic competition. All 
of the 83 major defense acquisition programs and the many smaller acquisition category II and III efforts that make up 
the other 65 percent of defense investment scattered across the 3,112 program, project, and activity (PPA) line items 
found in the president’s budget request now include some software activity by our accounting.<sup>2</sup> We would be 
thrilled if a larger community—contracting officers, industry executives, academics, engineers and programmers, policy 
analysts, legislators, staff, and operational military service members—also gleaned insight from this document. But we 
know that some terms may come across as jargon and that not everyone is familiar with the names of common software 
development tools or methods. We encourage them to read this nonetheless and are confident that the core principles and 
insights we present are still accessible to a broader audience.


While other recent analyses have focused on the imperative for software and offered high-level visions for a better 
future,<sup>3</sup> we believe most of the acquisition community already recognizes the potential of a digital future 
and is engaged in a more tactical set of battles and decisions: how to structure their organizations, how to manage 
expectations, how to structure their deliverables, and how to write solicitations and let contracts meet requirements 
and strive for useful outcomes. We attempt to present background and principles that can assist them in navigating this 
complex landscape.


The real motivation for getting military software right is not to make the DoD more like commercial industry through 
digital modernization. Instead, it is to create a set of competitive advantages for the United States that stem from 
the embrace of distributed decision-making and mission command. The strategic context of this work stems from the 
observation that advantage in future military contests is less likely to come from the mere presence of robotics or 
artificial intelligence in military systems and is more likely to come from using these (and other) components 
effectively as part of a force design, and specifically from maintaining sufficient adaptability in the creation and 
implementation of tactics. Software, software systems, and information processing systems (including artificial 
intelligence and machine learning, or AI/ML) that leverage software-generated data are the critical ingredients in 
future force design, force employment, tactics generation, and execution monitoring. Software will bind together human 
decision-makers and automation support in future conflict.


This report aims to accomplish two goals:

* Elucidate a set of principles that can help the acquisition community navigate the software world—a turbulent sea of buzzwords, technological change, bureaucratic processes, and external pressures.
* Recruit this community to apply energy to a handful of areas that will enable better decisions and faster actions largely built around an alternative set of processes for evolutionary development.

The report is structured in chapters, each built around a core insight. [Chapter 1](introduction.md) notes that the 
speed and ubiquity of digital information systems is driving military operations ever closer to capability development, 
and that this trend brings promise for capability and peril for bureaucratic practices.


[Chapter 2](adaptability.md) offers the military framing for software development, pointing out that it can enable 
greater adaptability in force employment and that the DoD cannot derive future concepts of more distributed forces and 
greater disaggregation of capability from requirements and specifications alone. Instead, software should enable 
employment tactics to evolve, especially as the elements of future combat are outside the control of any one program 
manager or office.


[Chapter 3](digital-logistics.md) introduces a framing analogy between software delivery and logistics. As logistics 
practitioners recognize, there is no one-size-fits-all solution to the problem of moving physical goods, but a set of 
principles that helps navigate many gradients of logistics systems. Similarly, the world of software is full of 
diversity—different use cases, computing environments, and security levels—and this heterogeneity is an intrinsic 
feature that the DoD needs to embrace.


[Chapter 4](modern-software-factory.md) introduces the essential tool of the modern program office—the software 
factory—the tooling and processes via which operational software is created and delivered. All existing operational 
software was made and delivered somehow and, whether we like it or not, we will have to update it in the future. Thus, 
the production process matters. In many ways, the most important thing a PEO can do is identify, establish, or source 
an effective software factory suited to the particular needs of their unique deliverables.


[Chapter 5](applied-software-acquisition.md) seeks to break down the ideas introduced earlier into actionable atomic 
principles that the DoD can use to navigate the tough decisions that the acquisition community faces; we refer to these 
ideas as ACTS. To aid the reader in understanding these, we also provide a [fictitious vignette](exercising-acts-vignette.md).


We recognize the inherent tension between making a report compact and accessible and covering the myriad facets of a 
broad and fast-changing scene. To balance this, we believe that we have focused this report on the most impactful 
aspects of software acquisition.

![The six ACTS and their corollaries in a clockwise circle](images/figure-1.png)