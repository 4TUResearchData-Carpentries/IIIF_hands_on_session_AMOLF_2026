- What are repositories for long term preservation of research data and software
    - Context and uses cases
- What is 4TU.ResearchData
- Main services we offered to reuse data from the repository
    - PID, DOI
    - API
    - IIIF
- Explain what is IIF 

Hands on session

- Deposit a group of images to the next.data.4tu.nl sandbox domain of 4TU.ResearchData
    - for the ones how dont have it they can use my images: https://next.data.4tu.nl/datasets/5d40e250-23bd-4a79-9626-6c9d6003c747/1
- Then , explore the IIIF manifest of each of their images with a IIIF viewer (https://manifest-editor.digirati.services/?tab=recent)
- if we have time then we can perform some python analysis of the deposited datasets , to show the concept that they dont need to download the image to inspect or analyse them 
    - idea: they could use this dashboard : https://iiifconference2026-mfe8jpx3urgrjz6dwdtzbk.streamlit.app/


summary:


In the context of increasingly digital and data-intensive research, **data and software repositories are becoming essential infrastructures for enabling the long-term preservation, discoverability, accessibility, and reuse of research outputs**. This is particularly relevant for research involving large image collections, such as **microscopy, medical imaging, remote sensing, or astronomical images**, where accessing and reusing data can be challenging because researchers often need to download and store very large files locally before they can inspect or analyse them. At **4TU.ResearchData**, a research data repository tailored to the natural and engineering sciences, we have implemented the **International Image Interoperability Framework (IIIF)** to improve the way deposited images can be accessed and reused. IIIF provides standardised web-based mechanisms that allow images to be explored, visualised, and accessed remotely without necessarily downloading the complete original files. In this seminar, we will discuss the role of research repositories in supporting reusable research data, introduce the main concepts behind IIIF, and explore how IIIF is implemented within 4TU.ResearchData. During the hands-on session, participants will deposit a small collection of images in the 4TU.ResearchData sandbox environment and experiment with accessing and visualising their own data through IIIF-compatible tools.


proposed agenda:

 | Time            | Session                                          | Content                                                                                                                                                                                                          |
| --------------- | ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **15:00–15:05** | **Welcome & context**                            | Why long-term access and reuse of research images matters, especially for microscopy and other large imaging datasets.                                                                                           |
| **15:05–15:15** | **Research data & software repositories**        | What repositories do: preservation, discoverability, persistent identification, citation and reuse. Brief examples relevant to imaging research.                                                                 |
| **15:15–15:22** | **4TU.ResearchData & services for reuse**        | Very short introduction to 4TU.ResearchData and the mechanisms that support reuse: **DOIs/PIDs, API and IIIF**. Keep DOI and API brief and use them mainly to position IIIF within the repository ecosystem.     |
| **15:22–15:30** | **What is IIIF?**                                | Introduce the core idea of IIIF and why it is useful for large image collections. Briefly explain the **Image API**, **Presentation API / Manifest**, and how external applications can reuse repository images. |
| **15:30–15:40** | **Break**                                        | 10 minutes.                                                                                                                                                                                                      |
| **15:40–15:55** | **Hands-on 1 — Deposit/access an image dataset** | Participants deposit a few images in the `next.data.4tu.nl` sandbox. Participants who do not have suitable images can use your prepared microscopy dataset. (maybe use filesender.surf.nl)                                                     |
| **15:55–16:15** | **Hands-on 2 — Explore the IIIF Manifest**       | Locate the IIIF Manifest associated with the dataset and open it in the Digirati Manifest Editor/viewer. Inspect images, metadata, canvases and IIIF image services.                                             |
| **16:15–16:25** | **Hands-on 3 — Reuse without downloading**       | Use the Streamlit dashboard, or a very short Python demonstration, to show that an image or image region can be accessed and inspected remotely through IIIF rather than downloading the complete dataset. (could be the example of colab from the iiif conference)      |
| **16:25–16:30** | **Wrap-up & discussion**                         | Recap the workflow and discuss how this approach might fit microscopy workflows at the Amsterdam Imaging Hub.                                                                                                    |
