# RISE RISC-V Developers Appreciation Pilot Program


# About

Bringing the RISC-V architecture on par with other architectures requires broader software support. RISE recognizes the scale of this challenge, and the critical role of the wider developer community plays in reaching this goal.

To accelerate progress, RISE launched the RFP (Request For Proposal) program in 2023, providing funding and support for large-scale projects. However, while the RFP program aids major initiatives, many smaller projects only need minor adjustments to be tested and deployed on RISC-V. 

To bridge this gap, RISE is introducing the RISC-V Developer Appreciation Pilot Program (the “Pilot Program**”**), which focuses on recognizing and supporting developers working on these smaller efforts, including porting, testing, and releasing on RISC-V.

The goal is to make RISC-V support an integral part of every developer’s workflow, positioning RISC-V as the standard platform for all projects. This initiative seeks to foster collaboration and celebrate the contributions of developers, driving momentum for the RISC-V ecosystem. 


# Overview

The Pilot Program recognizes the contributions of software communities and developers who port their projects to RISC-V, driving broader engagement and growth in the ecosystem. The program prioritizes enabling projects on RISC-V over maximizing performance, ensuring it becomes a supported standard within the software landscape. For more complex initiatives, the RFP program is better suited. 

The Pilot Program will run from October 2024 to March 2025, with a total budget of up to 50,000 EUR. All work submitted for recognition (each, a “Submission”) must be upstreamed, released, and publicly available. 

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
   <td>The software functions seamlessly with minimal to no porting required. The primary task involves incorporating linux-riscv64 into the building, testing, and release pipelines. 
   </td>
   <td>500€
   </td>
  </tr>
  <tr>
   <td>Large
   </td>
   <td>The sources require porting to RISC-V, which may involve integrating a linux-riscv64 specific backend and utilizing existing compiler intrinsics or inline assembly. Additionally, the testing and release pipelines must be updated to support linux-riscv64. 
   </td>
   <td>3000€
   </td>
  </tr>
</table>



# Projects

The Pilot Program is dedicated exclusively to “Open Source Software” (under an open source software license recognized by the Open Source Initiative).  Commercial projects are outside the scope of this program. RISE does not claim ownership rights to your Submission. 

You represent and warrant that your Submission is your own work, that you haven't submitted work done by another person or entity, and that you have the right to provide the Submission.


## Sizing Examples

Examples of small and large project Submissions are included below to enable you to size your project.


<table>
  <tr>
   <td><strong>Project</strong>
   </td>
   <td><strong>Link to contribution(s)</strong>
   </td>
   <td><strong>Sizing</strong>
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/xtensor-stack/xsimd">xsimd</a>: C++ wrappers for SIMD intrinsics and parallelized, optimized mathematical functions (SSE, AVX, AVX512, NEON, SVE))
   </td>
   <td><a href="https://github.com/xtensor-stack/xsimd/pull/979">https://github.com/xtensor-stack/xsimd/pull/979</a>
   </td>
   <td><strong>Large</strong>
<p>
·        The linux-riscv64 configuration was added to CI
<p>
·        It required significant development work to add an implementation based on RVV 1.0
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/shibatch/sleef">sleef</a>: SIMD Library for Evaluating Elementary Functions, vectorized libm and DFT
   </td>
   <td><a href="https://github.com/shibatch/sleef/pull/476">https://github.com/shibatch/sleef/pull/476 \
 https://github.com/shibatch/sleef/pull/477</a>
   </td>
   <td><strong>Large </strong>
<p>
·        The linux-riscv64 configuration was added to CI
<p>
·        It required significant development work to add an implementation based on RVV 1.0
<p>
·        It is a dependency of a few largely used projects that are of interest to RISE members
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/facebook/rocksdb">rocksdb</a>: A library that provides an embeddable, persistent key-value store for fast storage.
   </td>
   <td><a href="https://github.com/facebook/rocksdb/pull/12139">https://github.com/facebook/rocksdb/pull/12139</a>
<p>
<a href="https://github.com/evolvedbinary/docker-rocksjava/pull/2">https://github.com/evolvedbinary/docker-rocksjava/pull/2</a>
   </td>
   <td><strong>Small</strong>
<p>
·        The linux-riscv64 configuration was added to CI
<p>
·        Very little to no other development work was required
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/simdjson/simdjson">simdjson</a>: Parsing gigabytes of JSON per second : used by Facebook/Meta Velox, the Node.js runtime, ClickHouse, WatermelonDB, Apache Doris, Milvus, StarRocks
   </td>
   <td><a href="https://github.com/simdjson/simdjson/pull/2088">https://github.com/simdjson/simdjson/pull/2088</a>
   </td>
   <td><strong>Small</strong>
<p>
·        The linux-riscv64 configuration was added to CI
<p>
·        Very little to no other development work was required
<p>
·        [multiplier: x2] simdjson is the reference implementation for fast json parsing and is widely used by many other projects
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/apache/commons-crypto">commons-crypto</a>: Apache Commons Crypto
   </td>
   <td><a href="https://github.com/apache/commons-crypto/pull/264">https://github.com/apache/commons-crypto/pull/264</a>
   </td>
   <td><strong>Small</strong>
<p>
·        The linux-riscv64 configuration was added to CI
<p>
·        Very little to no other development work was required
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/netty/netty">Netty</a>: an event-driven asynchronous network application framework
   </td>
   <td><a href="https://github.com/netty/netty/pull/13670">https://github.com/netty/netty/pull/13670</a>
   </td>
   <td><strong>Small</strong>
<p>
·        The linux-riscv64 configuration was added to CI
<p>
·        Very little to no other development work was required
<p>
·        [multiplier: x2] Netty is the most widely used networking library in the Java ecosystem for any high-performance software that needs fast I/O
   </td>
  </tr>
  <tr>
   <td><a href="https://github.com/hyperxpro/Brotli4j">Brotli4j</a>: provides Brotli compression and decompression for Java.
   </td>
   <td><a href="https://github.com/hyperxpro/Brotli4j/pull/111">https://github.com/hyperxpro/Brotli4j/pull/111</a>
   </td>
   <td><strong>Small</strong>
<p>
·        The linux-riscv64 configuration was added to CI
<p>
·        Very little to no other development work was required
   </td>
  </tr>
</table>



# Submission Process

Before reaching out, please ensure that your project has been fully ported, tested, and released, as we do not review work that is still in progress. Your Submission must be publicly available and under an Open Source License. 

When your work is ready,  Please Submit your contribution in a new Issue on the[ RISE Developer Appreciation GitHub](https://github.com/Rise-dev-appreciation?tab=repositories)<span style="text-decoration:underline;"> </span>and include the following information:

* **Project Name and Description:** Provide a brief overview (1 to 5 sentences) highlighting your project’s community usage and its significance within the broader RISC-V software stack. 
* **Contribution Links:** Share links to your contributions that support your request. These contributions must be publicly accessible without requiring login or account creation. 
* **GitHub Profile Link:** Include a link to your GitHub profile.
* **Request Reward Size:** Specify the amount you are requesting and explain why. Please refer to the Size table for details on what is expected for each reward level. 

The more detailed and clear your submission, the faster and more efficiently RISE can process your request for Pilot Program recognition. 


# Submissions Review Process

RISE has complete discretion over whether to recognize Submissions or not. No contributor should expect recognition for their current or future contributions to an Open Source Software project.

The RISE Project will determine which contributions to recognize. The goal is to ensure that this process remains as transparent as possible. As this is a Pilot Program with a limited budget and timeframe, we will evaluate and incorporate feedback to facilitate learning and adapt for future variations of the program’s implementation. 

Only Submissions that integrate linux-riscv64 into the project’s standard testing and release processes will be considered for review. The goal is to ensure that software is widely available on RISC-V, with assessments based on the quality of testing and release availability.

RISE will not tolerate any abuse of the program. If any project or community encounters issues related to the Pilot Program, please contact info@riseproject.dev for resolution. 


## Payment Process

We will generally review your Submission and provide a response by the 15th of the month following your Submission. All payments will be processed through GitHub Sponsors, so a GitHub account is required to receive a financial recognition. Please note that only individuals and organizations participating in the[ GitHub Sponsors](https://github.com/sponsors) Program are eligible for rewards.

Payments will generally be issued in the first week of the month following submission approval.


# Public Recognition

RISE may publicly recognize developers who have been received recognition under the Pilot Program. RISE, at its discretion, may recognize your contribution on a website, blog and social media.


# Terms

* RISE reserves the right to change or terminate this Pilot Program at any time. Any Submission under the Pilot Program is subject to the program details and terms available at that time. 
* Do not undertake any contribution or work with an expectation of a recognition payment for a future Submission. This is a Pilot Program with a limited budget for reward payments. Once the budget has been exhausted, RISE will not make any additional recognition payments under this Pilot Program. Consequently, some qualifying Submissions may receive reduced recognition payments or no recognition payments at all. Therefore, it is possible that your Submission could qualify for a recognition payment, yet no recognition payment will be issued. RISE is not responsible for Submissions that we do not receive for any reason.
* RISE also reserves the right to refuse payment at its sole discretion if it believes a submission undermines the spirit of this Pilot Program or if making the recognition payment would be illegal. 
* If RISE determines that your Submission is eligible for a recognition payment, we will notify you and provide instructions for processing your payment. You also have the option to be recognized but choose to waive the recognition payment if you prefer not to receive a recognition payment. If you are unable or unwilling to accept a recognition payment, RISE reserves the right to rescind any recognition payment.
*  If you accept a recognition payment, you will be solely responsible for all applicable taxes related to that recognition payment
* All decisions made by RISE are final. If you do not receive a confirmation email after making your Submission, notify info@risedev.com to ensure your Submission was received.


# Eligibility

All participants must be eligible to use the GitHub Sponsor’s program, available at[ https://docs.github.com/en/site-policy/github-terms/github-sponsors-additional-terms](https://docs.github.com/en/site-policy/github-terms/github-sponsors-additional-terms)

GitHub Sponsors requires your compliance with additional eligibility and program terms related to any recognition payment, including age eligibility, taxes, fees, sanctions, and other terms which you must agree with prior to making any Submission.

Employees of RISE sponsoring companies are not eligible for a recognition payment.

It is your responsibility to comply with any policies that your employer may have that would affect your eligibility to participate in the Pilot Program. If you are participating in violation of your employer’s policies, you may be disqualified from participating or receiving any recognition payment. 

There may be additional restrictions on your ability to enter depending upon your local
