# GSoC-2024 @FalcoSecurity
<div align="center">
<img src="https://github.com/GLVSKiriti/GSoC-2024/blob/main/falco-gsoc-featured.jpg" alt="GSoC-logo"  width=600px>
</div>

# General Information 📝
- <b>Organization:</b> [CNCF](https://github.com/cncf) <br>
- <b>Project:</b> [Falco Event Generator](https://github.com/falcosecurity/event-generator) <br>
- <b>Title:</b> Upgrading event-generator and automating Falco performance testing
- <b>Implementation Idea:<b> [Declarative YAML file testing feature](https://hackmd.io/@aldolck/r1o9yU170) <br>
- <b>Mentee:</b> [GLVS Kiriti](https://github.com/GLVSKiriti) <br>
- <b>Mentors:</b> [Jason Dellaluce](https://github.com/jasondellaluce), [Aldo Lacuku](https://github.com/alacuku) 

# Description 📜
Falco is a real-time security tool designed to detect abnormal behaviours and security-related runtime events in Linux systems and the cloud. The event-generator is an utility within the Falco ecosystem that helps testing Falco’s detection capabilities. The tool also has benchmark capabilities that represent a building block of the Falco performance testing practices. However, the project received less attention than required in the past few years and would require some care and renovation. 

# Goals 🎯
This Google Summer of Code project proposes upgrading the event-generator to improve its testing and benchmarking capabilities, its reliability, and its consistency, and developing new Continuous Integration pipelines based on it. The end goal is to evolve the event-generator and make it the standard tool for systematically accessing the correctness and performance of Falco’s threat detection capabilities at every release and development cycle

# What changes I did ? 🚀

## List of the PRs that are created during GSoC period.
- Currently all this PRs are merged to [gsoc2024 branch](https://github.com/falcosecurity/event-generator/commits/gsoc2024)
- My forked repo of event-generator [repo](https://github.com/GLVSKiriti/event-generator)
- My expereince so far upto midterm [blog](https://falco.org/blog/gsoc-2024-midterm/)

| Pull Requests                                                       |           Status             | Description |
|:--------------------------------------------------------------------|:----------------------------:|:------------:|
| [#211](https://github.com/falcosecurity/event-generator/pull/211)   |     :purple_square:Merged       |  This PR marked the starting of the implementation of Declarative YAML file testing feature. Specifically in this PR added the yaml file parsing functionality, implemented host runner and added the structure for yaml file      |
| [#216](https://github.com/falcosecurity/event-generator/pull/216)   |     :purple_square:Merged       |   Added the container runner interface and implemented setup and clenup methods          |
| [#217](https://github.com/falcosecurity/event-generator/pull/217)   |     :purple_square:Merged       |   Implemented executestep method for the container runner and refactored the folder and file structure          |
| [#218](https://github.com/falcosecurity/event-generator/pull/218)   |     :purple_square:Merged       |   Added the required helper function for making syscalls which are requiered to trigger the stable rules          |
| [#219](https://github.com/falcosecurity/event-generator/pull/219)   |     :purple_square:Merged       |   Added the test command that connects with grpc api of running falco instance and validates whether a rule is triggered or not when we run the events using the declarative yaml file testing feature           |
| [#1343](https://github.com/falcosecurity/falco-website/pull/1343)   |     :purple_square:Merged       |   Added a blog post on the experience so far upto midterm |
| [#1342](https://github.com/falcosecurity/falco-website/pull/1342)   |     :purple_square:Merged       |   Fixed Some typos |



## List of the PRs that are created before selection of GSoC :gift:

|                         Pull Requests                          |            Status                | Description |
|:--------------------------------------------------------------:|:--------------------------------:|:-----------------------------------------------------------------------------------:|
| [#100](https://github.com/falcosecurity/event-generator/pull/100)  |    :purple_square:Merged     |   Corrected  a typo                                                                 |
| [#101](https://github.com/falcosecurity/event-generator/pull/101)  |    :purple_square:Merged     |  Added event for trigerring rule "Write below root"                                 |
| [#102](https://github.com/falcosecurity/event-generator/pull/102)  |    :purple_square:Merged     |   Added event for trigerring rule "Write below monitored dir"                       |
| [#103](https://github.com/falcosecurity/event-generator/pull/103)  |    :purple_square:Merged     |   Added event for trigerring rule "Create hidden file or directory"                 |
| [#108](https://github.com/falcosecurity/event-generator/pull/108)  |    :purple_square:Merged     |      Added event for trigerring rule "Read shell configuration"                     |
| [#109](https://github.com/falcosecurity/event-generator/pull/109)  |    :purple_square:Merged     |     Added event for trigerring rule "Remove bulk data from disk"                    |
| [#112](https://github.com/falcosecurity/event-generator/pull/112)  |    :purple_square:Merged     |    Added event for trigerring rule "Read SSH information"                           |
| [#117](https://github.com/falcosecurity/event-generator/pull/117)  |    :purple_square:Merged     |    Added event for trigerring rule "Adding SSH keys to authorized_keys "            |
| [#122](https://github.com/falcosecurity/event-generator/pull/122)  |    :purple_square:Merged     |     Added event for trigerring rule "Program run with disallowed http proxy env"    |
| [#124](https://github.com/falcosecurity/event-generator/pull/124)  |    :purple_square:Merged     |     Added event for trigerring rule "Find AWS credentials "                         |
| [#125](https://github.com/falcosecurity/event-generator/pull/125)  |    :purple_square:Merged     |     Added event for trigerring rule "Execution from /dev/shm "                      |
| [#126](https://github.com/falcosecurity/event-generator/pull/126)  |    :purple_square:Merged     |    Fix broken links in readme                                                       |
| [#133](https://github.com/falcosecurity/event-generator/pull/133)  |    :purple_square:Merged     |     Added event for trigerring rule "PTRACE attached to process"                    |
| [#136](https://github.com/falcosecurity/event-generator/pull/136)  |    :purple_square:Merged     |     Added event for trigerring rule "PTRACE anti-debug attempt "                    |
| [#141](https://github.com/falcosecurity/event-generator/pull/141)  |    :purple_square:Merged     |     Added event for trigerring rule "Fileless execution via memfd_create "          |
| [#143](https://github.com/falcosecurity/event-generator/pull/143)  |    :purple_square:Merged     |     Added event for trigerring rule "Clear log activites "                          |
| [#156](https://github.com/falcosecurity/event-generator/pull/156)  |    :purple_square:Merged     |    Added event for trigerring rule "Polkit local privilege escalation vulnerability(CVE-2021-4034)"|
| [#157](https://github.com/falcosecurity/event-generator/pull/157)  |    :purple_square:Merged     |     Added event for trigerring rule "Sudo potential privilege escalation "          |
| [#161](https://github.com/falcosecurity/event-generator/pull/161)  |    :green_square: Open       |     Added event for trigerring rule "Linux kerenel module injection detected "      |
| [#163](https://github.com/falcosecurity/event-generator/pull/163)  |    :purple_square:Merged     |      Added event for trigerring rule "set setuid or setgid bit "                    |
| [#165](https://github.com/falcosecurity/event-generator/pull/165)  |    :purple_square:Merged     |     Added event for trigerring rule "Launch ingress remote file copy tools in container " |
| [#169](https://github.com/falcosecurity/event-generator/pull/169)  |    :purple_square:Merged     |     Added event for trigerring rule "Kubernetes Client Tool Launched in container"        |
| [#171](https://github.com/falcosecurity/event-generator/pull/171)  |    :purple_square:Merged     |    Added event for trigerring rule "Unprivileged Delegation of page faults handling to a userspace process"|
| [#173](https://github.com/falcosecurity/event-generator/pull/173)  |    :purple_square:Merged     |    Added event for trigerring rule "Detect crypto miners using srtatum protocol"          |
| [#176](https://github.com/falcosecurity/event-generator/pull/176)  |    :green_square: Open       |    Added event for trigerring rule "Detect outbound connections to common miner pool ports"      |
| [#182](https://github.com/falcosecurity/event-generator/pull/182)  |    :purple_square:Merged     |    Added event for trigerring rule "Container drift detected using chmod"                 |
| [#189](https://github.com/falcosecurity/event-generator/pull/189)  |    :purple_square:Merged     |    Added event for trigerring rule "Container drift detetced (open+create)"               |
| [#190](https://github.com/falcosecurity/event-generator/pull/190)  |    :purple_square:Merged     |    Added event for trigerring rule "Launch package management process in container"       |
| [#196](https://github.com/falcosecurity/event-generator/pull/196)  |    :purple_square:Merged     |     Added event for trigerring rule "Drop and execute new binary in container"            |
| [#202](https://github.com/falcosecurity/event-generator/pull/202)  |    :purple_square:Merged     |     Refactor in existing event to use events.ErrSkipped with a proper reason when skippinf an actions|
| [#203](https://github.com/falcosecurity/event-generator/pull/203)  |    :purple_square:Merged     |    Added event for trigerring rule "Detect release_agent file container escapes"          |
| [#208](https://github.com/falcosecurity/event-generator/pull/208)  |    :purple_square:Merged     |     Bug fix in execution dev shm event                                                    |
| [#83](https://github.com/falcosecurity/plugin-sdk-go/pull/83)      |    :purple_square:Merged     |     Added a job in ci which builds the all examples in plugin-sdk-go repo                 |
| [#48](https://github.com/falcosecurity/testing/pull/48)            |    :green_square:Open        |     Added Test for falco -h and falco --help commands in testing repo                     |



# What are the remaining tasks ? 🗣️
  - Improving benchmarking capabilities of event-generator
  - Integrate the enhanced event-generator in falco-ci pipleine

# Future Plans: ⏲️
Following GSoC, I’m eager to maintain the same level of contribution and further engage with the community. I look forward to supporting new developers and exploring both new and existing projects within the organization. I am committed to being as helpful as possible to the community moving forward. 😇 If anyone needs assistance or wishes to connect, I’m just a couple of clicks away.

# Conclusion 👏
I want to extend my heartfelt thanks to my mentors ❤️, Jason Dellaluce and Aldo Lacuku, for their unwavering support throughout my GSoC journey. Their patience and invaluable suggestions were crucial whenever I encountered challenges. I also appreciate the entire Falco community, especially Leonardo Grasso and Federico Di Pierro, for their exceptional assistance during the GSoC selection process. All of your help was instrumental in making this experience a success 🔥.


