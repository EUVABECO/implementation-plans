# ELECTRONIC PATIENT INFORMATION LEAFLET (ePIL) - DATA

# Patient Information Leaflets

The exposure of the ePIL to citizens and to health professionals requires that these documents are existing and accessible.

This is today only partially true:

-   The [EMA database for centrally approved products](https://www.ema.europa.eu/en/medicines) is comprehensive but exposes single PDF documents that gather the summary of product characteristics, the labels and the patient information leaflet. These documents are massive (hundreds of pages) and hardly accessible to non-specialists.
-   Standalone ePIL can be found on several national authorities’ portals, but only for locally approved vaccines.
-   The new EMA Product Lifecycle Management portal would provide the product information in a semi-structured way, allowing to recompose the ePIL. At the time of writing (Apr. 2026) its content is limited to 24 medicines, and only one vaccine, but the recently published [ePI roadmap](https://www.ema.europa.eu/en/documents/other/electronic-product-information-epi-roadmap_en.pdf) indicates that further vaccines could be incorporated on a voluntary basis from the last quarter of 2026.

# Other vaccine related information

The mechanisms described in this implementation for accessing the Patient Information Leaflet could be reused for a variety of other vaccine related documents, such as:

-   Summary of Product Characteristics
-   Pharmacovigilance alerts
-   Synthetic disease related information (similar to the Vaccine Information Statements released by the US CDC).

The PLM portal is today the best approximation of a content management system for vaccines. Yet, even if contains structured content, this structure is only a representation of the aspect of the document (sections, figures, etc). Ideally a future version would have a semantically significant structure, allowing to generate adequate documentations for different audiences and automated processes, such as the automated extraction and check of contraindications against a patient health record.
