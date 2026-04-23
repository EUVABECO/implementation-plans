# ELECTRONIC PATIENT INFORMATION LEAFLET (ePIL) - VERIFICATION

## Verification of the trusted directory

The points to be checked are:

-   The security of access to the trusted directory
-   The correct format of the references file

The security of access to the trusted directory depends upon the feeding process defined during the implementation. Its verification should cover organisational measures (on the accreditation process and distribution of authentication means) and technical measures. It should at least include a penetration test by a qualified auditor.

Yet, this verification may be generic to the institutional server presenting the trusted directory. If its security is already assessed globally, this assessment can be reused without further actions.

The correct format of the references file is checked indirectly through the correct generation of the redirection server configuration.

## Verification of the redirection server

The points to be checked are:

-   The availability of the redirection server.
-   The regular execution of the regeneration of the redirection server configuration.

Serving static redirections is a very lightweight process. An overload of the redirection server is highly unlikely, but a system failure is always possible. To keep the redirections available, simple redundancy mechanisms, such as load balancing or delegation to a robust Content Delivery Network (CDN), should be implemented.

If the redundancy is implemented within the ePIL infrastructure, failure scenarios should be tested. If it relies upon an external CDN service, the performance of the CDN provider should be assessed by long-term monitoring data.

## Verification of the access tools

For each access tool, the verification process should include:

-   The check that an update in the trusted directory is propagated to the user interface within a determined time lapse (typically less than one day).
-   If a renderer is included into the access tool, the check that the rendering includes all of the data present in the ePIL, including all sections and graphical elements.
