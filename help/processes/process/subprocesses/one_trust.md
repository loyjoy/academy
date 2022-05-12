## OneTrust integration

Create or update a consent receipt in OneTrust or retrieve the status of a consent receipt for a customer.

### Retrieve the status for a consent receipt

**Process variable** save the purpose status of the consent receipt. The purpose status can take the following values: *ACTIVE, ALWAYS_ACTIVE, EXPIRED, EXTEND, HARD_OPT_OUT, NONE, NO_CONSENT, OPT_OUT, PENDING, WITHDRAWN*.

**Customer** app-{env} e.g. app-eu.

**Client ID** and **API secret** OneTrust credentials used to create an access token. Further information can be found in the OneTrust documentation: https://developer.onetrust.com/docs/api-docs-v3/b3A6MjI4OTUyOTc-generate-access-token.

**Collection Point ID** and **Purpose ID** IDs to filter the list of consent receipts.

For further information regarding the fields see the OneTrust documentation: https://developer.onetrust.com/docs/api-docs-v3/b3A6MjI4OTU0Nzg-get-a-paged-list-of-data-subjects-and-associated-data-elements-sorted-in-descending-order-of-last-modified-date-by-default.

### Create or update a consent receipt

**Customer** privacyportal-{env} e.g. privacyportal-eu.

**Collection Point JWT token** access token to the collection point.

**Purpose ID** specifies the purpose for which the status should be changed.

**Purpose status** change the purpose status of the existing or newly created consent receipt to one of the following values: *CANCEL, CHANGE_PREFERENCES, CONFIRMED, EXPIRED, EXTEND, HARD_OPT_OUT, NOTGIVEN, NO_CHOICE, OPT_OUT, PENDING, WITHDRAWN*.

For further information regarding the fields see the OneTrust documentation: https://developer.onetrust.com/docs/api-docs-v3/b3A6MjI4OTU0OTU-create-receipts-from-a-collection-point. 
