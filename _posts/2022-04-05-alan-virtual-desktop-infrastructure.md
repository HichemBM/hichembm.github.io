---
layout: post
title: "My Fix for a Windows App in a Mac World"
date: 2022-04-05
categories: Alan
author_name: Hichem
author_url: /about/
author_avatar: hichem
feature_image: alan-office-1
---
*Delivering Windows applications on macOS, Anywhere.*

Managing a completely homogeneous IT environment, like the all-MacBook fleet I oversaw as the first IT Manager at [Alan](https://alan.com), has its perks. Onboarding is streamlined, support is simpler, and you can build deep expertise on one platform. But every so often, you hit a wall, an edge case that challenges the entire setup.

For us, that moment came when a key team required a specific piece of compliance software. The catch? It was only available for Windows. This wasn't just a user preference; it was a **critical business need**. The challenge was to introduce a Windows environment into our Apple ecosystem without disrupting our user-centric, hybrid-first work culture.

---

## Evaluating the Paths Forward

My task was to find a solution that was secure, scalable, and didn't place an undue burden on the end-user. I explored three main options:

1.  **Local Virtualization**: Installing a tool like *Parallels* or *VMware* on the user's MacBook. This is a quick fix, but it comes at the cost of performance, consuming significant RAM and CPU resources on the host machine.
2.  **A Dedicated Physical PC**: We could have purchased a Windows laptop. However, Alan operates on a hybrid model. Asking an employee to juggle two separate machines, especially when moving between home and various office spaces, was a non-starter. It just wasn't practical.
3.  **Cloud-Based Virtual Desktop Infrastructure (VDI)**: Providing a persistent virtual desktop hosted in the cloud that the user could access from anywhere, on any device.

The VDI approach quickly became the front-runner. It offered the flexibility our hybrid model demanded and avoided any performance impact on the user's primary device. The goal was to provide a seamless experience, not a technical workaround.

## Choosing the Right Tool: Pragmatism Over Preference

With VDI selected as the strategy, the next step was choosing a platform. My initial preference was Google Cloud Platform (GCP), as our entire internal IT stack was built on Google Workspace. Integrating with our existing user groups and identity management would have been ideal. However, at the time, GCP's compute offerings were limited to *Windows Server*, not the desktop experience we needed.

This led me to **Amazon Web Services (AWS)** and their **[Amazon WorkSpaces](https://aws.amazon.com/workspaces/)** service.

The decision to use AWS was a pragmatic one. Alan’s engineering team already had a robust and secure AWS infrastructure in place. By tapping into their environment, I could leverage existing security protocols, network configurations, and, most importantly, a wealth of in-house expertise. It meant I wasn't building a solution in a silo; I was integrating it into a **proven, well-managed cloud ecosystem**.

## The Result: An Immediate and Lasting Impact

The implementation was straightforward. After deploying the virtual desktop, I ran a brief training session with the team lead. He was able to install his specialized software and get to work almost immediately. The solution gave his team the freedom to access their critical Windows tools from their MacBooks, whether they were at home, in the office, or traveling.

The true measure of success, for me, often comes long after a project is completed. About four years later, I attended a company event and had a chat with that same person. He brought up the VDI project and mentioned how valuable it had been for his team's workflow over the years.

This project was a perfect example of how the right technical solution is about more than just technology. It’s about **understanding user needs, aligning with company culture, and pragmatically using the resources and expertise already at your disposal**. It's about finding a solution that doesn't just work today, but continues to provide value for years to come.

---

**What are your thoughts on using VDI for specific use cases like this?**\
Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/hichem-bm/){:target="_blank" rel="noopener noreferrer"} to discuss further!
