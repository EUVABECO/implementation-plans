# ELECTRONIC PATIENT INFORMATION LEAFLET (ePIL)  - DEPLOYMENT

# Project team

The project team will consist of:

-   NCA representants, for the feeding process and possibly updates to their own information system.
-   Software developers for the customer facing tools
-   Technical team for the infrastructure
-   A legal advisor for establishing the needed contracts

# Workflow

It is considered here that the ePIL documents exist as online resources, either as finalised PDF documents or as structured resources available for the assembly of a document.

The project team should then:

-   Determine the instantiated architecture
-   Implement the trusted directory of references
-   Organise its maintenance by the National competent authority
-   Implement the redirection server
-   Implement the tools for access by citizens

## Determine the instantiated architecture

The team should make decisions:

-   The online location for the public exposition of the machine-readable format for the references. This is a simple static file, that should be made freely available online to any consuming tool. Yet, this content must be secured against unauthorised modification or fraudulent substitution.
-   The access control mechanisms, making sure that only accredited individuals or systems from the NCA can update the references.
-   The process for the accredited individuals or systems to perform this update.
-   The technology and the base URL for the redirection server, as well as the automated process to configure it from the references file.
-   The mechanisms proposed to citizens to access to the ePIL. The three access modes listed in the architecture module (from the vaccine package, from personal health records, or from a list of authorized vaccines) should be considered.

The use of indirect references, for example in the case of centrally approved projects, requires that redirection servers also exist for the originating health jurisdictions. Rather than relying upon such servers provided by others, it is suggested that the redirection server should also generate the redirection maps based upon the references file of the originating health jurisdiction.

If such a reference file does not exist yet, the team could decide to temporarily create it on its own. It will not be less appropriate than the current situation and paves the way for a future compliant publication.

## Implement the trusted directory of references

The trusted directory of references for a country is a single, static file that can be exposed from any robust institutional website. The implementation will consist in:

-   Building a first version of the file, based upon the currently authorised vaccines and the relevant documents identified by the NCA.
-   Determining a feeding process to expose this file on the institutional website.
-   If needed, also build a temporary redirection file for other health jurisdictions.

The feeding process should include a version control mechanism, allowing to identify and track the changes across successive versions of the references file.

Submitting a new file should be subject to an authentication with an accredited account. Standard authentication protocols, such as client certificates and signed identity tokens, are totally applicable.

## Organise the maintenance of references

The updating of references must be a built-in process within the existing marketing authorization process.

The reference files are in an explicit format (YAML) that can be easily edited by hand, but it could be interesting for routine use to include their update into the production tools of the NCA.

It is also possible to allow the vaccine manufacturer themselves to expose their own redirection servers, and to reference these from the references file of the implementing Member State.

The organisation of the maintenance of references can then adopt several approaches:

-   If the references file is to be edited by hand, the responsible persons within the NCA should be identified, accredited and trained.
-   If it is generated and pushed from an automated process, this implies a new development within the NCA own information system. The specification for the file format is available from the build resources; the transfer method will have to be documented based upon the feeding process adopted in the implementation of the trusted directory.
-   If part of the update is delegated to the vaccine manufacturers through their own redirection server, this has to be included into contracts between the NCA and the manufacturers.

## Implement the redirection server

The redirection server replies to requests according to standardized format, such as:

<https://epil.euvabeco.eu/EUE/VAC0005/1/ePIL/fr>

by a redirection to the associated resource, that is either the ePIL document by itself or a standardised URL towards another redirection server.

It does not imply software development, but only the configuration of a Web server with redirection rules. The redirection server does not have to expose any content on its own, and avoiding such expositions will secure it against most cyberattacks.

The configuration file can be generated automatically from the references file. An [example implementation](https://github.com/EUVABECO/epil/blob/main/.github/workflows/generate-htaccess.yml) generating a configuration for an Apache server is shared with the build resources.

Thus, the setup of the redirection server only requires:

-   To implement the generation of the Web server configuration
-   To expose a faceless Web server, with an automated update of its configuration from the generated Web server configuration.

Such a server has been implemented for the EUVABECO project, serving redirections from references files for Belgium, France, Luxembourg, Latvia, Poland and centrally approved vaccines with the base URL <https://epil.euvabeco.eu>

## Implement the tools for access by the citizens

In all three access modes, the ePIL is exposed through a Web browser, either integrated into the application used by the citizen or invoked from this application. This browser has to support redirection and should preferably be able to display of PDF documents.

The difference between the access modes only lies into the way the used reference is identified.

When reading from the package, the application should have access to a map between the DCI included in the DataMatrix and the vaccine product identification. This mapping can only be established by the vaccine manufacturer. This information is already transmitted to the Medicines Verification Organisation instituted by the Falsified Medicines Directive, but its use for referencing the ePIL has no legal basis so far.

When reading from a health record of administered or prescribed vaccines, the mapping from the codes used within the application and the vaccine product code used in the standardised reference relies upon the NUVA alignment files, also used to populate the EVC.

Listing all the vaccines from a references file and proposing links to the associated documents is a simple and straightforward process. A [basic implementation](https://epil.euvabeco.eu/list_epil) has been delivered within the EUVABECO project.

# Typical planning

The overall planning could thus be as follows:

| Task                                           | M1 | M2 | M3 | M4 | M5 | M6 |
|------------------------------------------------|----|----|----|----|----|----|
| Determine the instantiated architecture        |  X |    |    |    |    |    |
| Implement the trusted directory of references  |    |  X |    |    |    |    |
| Organise the maintenance of references         |    |    |  X |  X |    |    |
| Implement the tools for access by the citizens |    |    |    |  X |  X |  X |

# Build resources

The EUVABECO project has exposed within a [GitHub repository](https://github.com/EUVABECO/epil):

-   References files for several countries,
-   The tool for generating the redirection server configuration for an Apache server
-   The Web site pages with client-side scripts for:
    -   Listing all ePILs from the reference files (list_epil)
    -   Listing a subset of ePILs from the reference files (view_epil)
    -   Listing all documents from the PLM portal (list_plm)
    -   Rendering a document from the PLM portal (view_plm)

A Web site serving both as the redirection server and as a navigation portal has been deployed at <https://epil.euvabeco.eu>
