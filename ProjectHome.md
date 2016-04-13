django-webfaction is intended to provide a simple control panel for creating and modifying email addresses and mailboxes for sites that use Webfaction shared hosting. It seamlessly integrates into the Django admin and emails are listed and edited as if they were Django models (although no model is stored apart from the logging of changes).

It was developed the match my specific requirements and therefore currently imposes the following constraints:

  * The distinction between email addresses and mailboxes is partly hidden from users to keep things simple. They create an email address with either a redirect address, a mailbox or both
  * Therefore users can have only one mailbox and/or one redirect address per email address
  * No support for deleting email accounts or mailboxes
  * No support for adding a mailbox except when an email address is first created (redirects can be added afterwards)
  * Certain naming conventions are imposed to allow automatically naming mailboxes. Specifically each domain that users are allowed to create addresses for has a prefix defined. The mailbox is created from the prefix and (kind of) 'slugified' version of the email address