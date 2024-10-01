

# RISE RISC-V Developer Appreciation Pilot Program


# About

Bringing the RISC-V architecture on par with other architectures requires broader software support. RISE recognizes the scale of this challenge and the critical role of the wider developer community plays in reaching this goal.

To accelerate progress, RISE launched the RFP (Request For Proposal) program in 2023, providing funding and support for large-scale projects. However, while the RFP program aids major initiatives, many smaller projects only need minor adjustments to be tested and deployed on RISC-V. 

To bridge this gap, RISE is introducing the RISC-V Developer Appreciation Pilot Program (**Pilot Program**), which focuses on recognizing and supporting developers working on these smaller efforts, including porting, testing, and releasing on RISC-V.

The goal is to make RISC-V support an integral part of every developer’s workflow, positioning RISC-V as the standard platform for all projects. This initiative seeks to foster collaboration and celebrate the contributions of developers, driving momentum for the RISC-V ecosystem. 


# Overview

Drawing inspiration from the success of  security bug bounty programs by companies like [Google](https://bughunters.google.com/about/rules/google-friends/6625378258649088/google-and-alphabet-vulnerability-reward-program-vrp-rules) and [Microsoft](https://www.microsoft.com/en-us/msrc/bounty-terms?rtc=1), we are adopting a more proactive approach. Rather than focusing on individual  projects, we aim to recognize and appreciate the efforts of the software communities and developers who actively port their projects to RISC-V, fostering broader engagement and growth within the ecosystem. 

The RISE RISC-V Developer Appreciation Pilot Program aims to prioritze enabling projects on RISC-V over maximizing performance, ensuring that RISC-V becomes a standard in the software ecosystem. For more complex efforts the RFP program is better suited.  

The Pilot program will run from October 2024 to March 2025, with a total budget of up to 50,000 EUR. All submitted work must be upstreamed, released, and publicly available. 

Contributions will be categorized based on the estimated effort required for each project’s porting. 


<table>
  <tr>
   <td>Category
   </td>
   <td>Completed work
   </td>
   <td>Reward
   </td>
  </tr>
  <tr>
   <td>Small
   </td>
   <td>The software functions seamlessly with minimal to no porting required. The primary task involves incorporating <code>linux-riscv64</code> into the building, testing, and release pipelines. 
   </td>
   <td>500€
   </td>
  </tr>
  <tr>
   <td>Large
   </td>
   <td>The sources require porting to RISC-V, which may involve integrating a <code>linux-riscv64</code> specific backend and utilizing existing compiler intrinsics or inline assembly. Additionally, the testing and release pipelines must be updated to support <code>linux-riscv64</code>. 
   </td>
   <td>3000€
   </td>
  </tr>
</table>



# Projects

The Pilot Program is dedicated exclusively to Open Source Software.  Commercial projects are outside the scope of this program. RISE does not claim ownership rights to your Submission. 

Represent and warrant that your Submission is your own work, that you haven't used information owned by another person or entity, and that you have the right to provide the Submission.


## Sizing Examples

Below includes an example of a small and a large project to enable you to size your project.


<table>
  <tr>
   <td>Project
   </td>
   <td>Link to contribution(s)
   </td>
   <td>Sizing
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/xtensor-stack/xsimd">xsimd</a>: C++ wrappers for SIMD intrinsics and parallelized, optimized mathematical functions (SSE, AVX, AVX512, NEON, SVE))
   </td>
   <td><a href="https://github.com/xtensor-stack/xsimd/pull/979">https://github.com/xtensor-stack/xsimd/pull/979</a>
   </td>
   <td><strong>Large</strong>
<p>
- The linux-riscv64 configuration was added to CI
<p>
- It required significant development work to add an implementation based on RVV 1.0
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/shibatch/sleef">sleef</a>: SIMD Library for Evaluating Elementary Functions, vectorized libm and DFT
   </td>
   <td><a href="https://github.com/shibatch/sleef/pull/476">https://github.com/shibatch/sleef/pull/476</a> \
<a href="https://github.com/shibatch/sleef/pull/477">https://github.com/shibatch/sleef/pull/477</a>
   </td>
   <td><strong>Large </strong>
<p>
- The linux-riscv64 configuration was added to CI \
- It required significant development work to add an implementation based on RVV 1.0
<p>
- It is a dependency of a few largely used projects that are of interest to RISE members
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/facebook/rocksdb">rocksdb</a>: A library that provides an embeddable, persistent key-value store for fast storage.
   </td>
   <td><a href="https://github.com/facebook/rocksdb/pull/12139">https://github.com/facebook/rocksdb/pull/12139</a>
<p>
<a href="https://github.com/evolvedbinary/docker-rocksjava/pull/2">https://github.com/evolvedbinary/docker-rocksjava/pull/2</a>
   </td>
   <td><strong>Small \
</strong>- The linux-riscv64 configuration was added to CI \
- Very little to no other development work was required
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/simdjson/simdjson">simdjson</a>: Parsing gigabytes of JSON per second : used by Facebook/Meta Velox, the Node.js runtime, ClickHouse, WatermelonDB, Apache Doris, Milvus, StarRocks
   </td>
   <td><a href="https://github.com/simdjson/simdjson/pull/2088">https://github.com/simdjson/simdjson/pull/2088</a>
   </td>
   <td><strong>Small  \
</strong>- The linux-riscv64 configuration was added to CI \
- Very little to no other development work was required \
- [multiplier: x2] simdjson is the reference implementation for fast json parsing and is widely used by many other projects
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/apache/commons-crypto">commons-crypto</a>: Apache Commons Crypto
   </td>
   <td><a href="https://github.com/apache/commons-crypto/pull/264">https://github.com/apache/commons-crypto/pull/264</a>
   </td>
   <td><strong>Small \
</strong>- The linux-riscv64 configuration was added to CI \
- Very little to no other development work was required
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/netty/netty">Netty</a>: an event-driven asynchronous network application framework
   </td>
   <td><a href="https://github.com/netty/netty/pull/13670">https://github.com/netty/netty/pull/13670</a>
   </td>
   <td><strong>Small  \
</strong>- The linux-riscv64 configuration was added to CI \
- Very little to no other development work was required \
- [multiplier: x2] Netty is the most widely used networking library in the Java ecosystem for any high-performance software that needs fast I/O
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/hyperxpro/Brotli4j">Brotli4j</a>: provides Brotli compression and decompression for Java.
   </td>
   <td><a href="https://github.com/hyperxpro/Brotli4j/pull/111">https://github.com/hyperxpro/Brotli4j/pull/111</a>
   </td>
   <td><strong>Small \
</strong>- The linux-riscv64 configuration was added to CI \
- Very little to no other development work was required
   </td>
  </tr>
</table>



# Submission Process

Before reaching out, please ensure that your project has been fully ported, tested, and released, as we do not review work that is still in progress. Your submission must be publicly available and it is under a Open Source License. 

When your work is ready,  Please fill out RISE RISC-V Appreciation Pilot Program Submission and include the following information:



* **Project Name and Description:** Provide a brief overview (1 to 5 sentences) highlighting your project’s community usage and its significance within the broader RISC-V software stack. 
* **Contribution Links:** Share links to your contributions that support your request. These contributions must be publicly accessible without requiring login or account creation. 
* **GitHub Profile Link:** Include a link to your GitHub profile.
* **Request Reward Size:** Specify the amount you are requesting and explain why. Please refer to the Size table for details on what is required for each reward level. 

The more detailed and clear your submission, the faster and more efficiently RISE can process your request. 

Please submit by the 15th of the month, and you will receive a response by the 30th. If you miss this deadline, no worries—you can always submit in the next cycle. Payments will be issued in the first week of the month following submission approval.


# Submissions Review Process

RISE has complete discretion to accept or reject submissions. 

The RISE Project will determine which contributions are eligible for rewards. The goal is to ensure that this process remains as transparent and predictable as possible. As this is a Pilot Program with a limited budget and timeframe, we will evaluate and incorporate feedback to facilitate learning and adapt for the final program implementation. 

Only contributions that integrate `linux-riscv64` into the project’s standard testing and release processes will be considered for review. The goal is to ensure that software is widely available on RISC-V, with assessments based on the quality of testing and release availability.

RISE will not tolerate any abuse of the program. If any project or community encounters issues related to the Pilot Program, please contact [info@riseproject.dev ](mailto:info@riseproject.dev) for resolution. 


# Payment Process

We will review your submission and provide a response by the 15th of the month following your submission. Payments will be processed through GitHub Sponsors, so a GitHub account is required to receive the reward. Please note that only individuals and organizations participating in the [GitHub Sponsors](https://github.com/sponsors)  Program are eligible for rewards.

Payments will be issued in the first week of the month following submission approval.


# Public Recognition 

RISE may publicly recognize developers who have been awarded. RISE at its discretion may recognize you on website, blog and social media unless you explicitly ask us not to include your name.

Badges will be awarded to contributors for accepted submissions. Badges are issued via Credly for use on your socials.


# Terms



* RISE reserves the right to change or terminate this Pilot Program at any time. By participating in this Pilot Program after any changes take effect, you agree to these changes. 
* This is a Pilot Program with a limited budget for reward payments. Once the budget has been exhausted, RISE will not make any additional payments under this Pilot Program. Consequently, some qualifying submissions may receive reduced rewards or no reward payments at all. Therefore, it is possible that your submission could qualify for a reward, yet no payment is issued.
* RISE also reserves the right to refuse payment at its sole discretion if it believes a submission undermines the spirit of this Pilot Program or if making the reward payment would be illegal. 
* If RISE determines that your submission is eligible for a reward, we will notify you and provide instructions for processing your payment. You may choose to waive the payment if you prefer not to receive a reward. If you are unable or unwilling to accept a reward, RISE reserves the right to rescind it.
* If you accept a reward payment, you will be solely responsible for all applicable taxes related to that payment.
* All decisions made by RISE are final. RISE is not responsible for Submissions that we do not receive for any reason. If you do not receive a confirmation email after making your submission, notify [info@risedev.com](mailto:infor@risedev.com) to ensure your Submission was received


# Eligibility 

You **<span style="text-decoration:underline;">ARE</span>** eligible to participate in the Pilot Program if you meet the following criteria: 



* You are 14 years of age or older. If you are at least 14 years old but are considered a minor in your place of residence, you must obtain your parent's or legal guardian's permission prior to participating in this Program. 
* You are an individual participating in your own individual capacity, or you work for an organization that permits you to participate. You are responsible for reviewing your employer's rules for participating in this Program.

You **<span style="text-decoration:underline;">ARE NOT</span>** eligible to participate in the Pilot Program if you meet any of the following criteria: 



* You are a resident of any countries under U.S. sanctions (see link for current sanctions list posted by the United States Treasury Department) or any other country that does not allow participation in this type of program;
* You are under the age of 14.
* Your organization does not allow you to participate in these types of programs.
* You are currently an employee of a RISE Sponsor company.

It is your responsibility to comply with any policies that your employer may have that would affect your eligibility to participate in the Program. If you are participating in violation of your employer’s policies, you may be disqualified from participating or receiving any payment. 

There may be additional restrictions on your ability to enter depending upon your local law.
