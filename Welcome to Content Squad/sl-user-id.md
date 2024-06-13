# SoftLayer User Identifiers

When working on SoftLayer deliverables, you will likely need two different
SoftLayer User IDs:
1. An internal development ID, usually composed of your first
initial followed by last name (such as sbaumann)
    - Used to gain access to the
    SoftLayer internal network via the SoftLayer VPN (requires Symantec VIP
    for two factor authentication)
    - Used for the SoftLayer Atlassian tools such as Jira and Confluence
    - Used to access the [SoftLayer internal employee portal](https://internal.softlayer.com/)
2. An external SoftLayer ID, typically in the format of "_username-sl_"
(e.g. jjfall-sl)
    - Used to order, manage and cancel SoftLayer devices at the
    [SoftLayer Control portal](https://control.softlayer.com/)
    (unless you have migrated your SoftLayer user account to use IBM ID)
    - Used to open tickets for devices owned by the account
    - Used in one of your workstation set up files to specify the authenticated
    user that is used to call jumpgate CLI

## Getting Help
281-714-4500 - Softlayer Helpdesk

## Creating Your Internal SoftLayer Account

Your internal SoftLayer account is used to access the SoftLayer VPN and to
access the Atlassian tools such as Jira and Confluence. Your first line manager
must request an internal development SoftLayer user ID for you.

After your manager requests a development SoftLayer user account, you will
receive an email from the SoftLayer help desk with instructions for enabling
your internal SoftLayer account and establishing a VPN connection to the
SoftLayer internal network.  See the [SoftLayer VPN](sl_vpn.md) section for
more information.


## Creating Your External SoftLayer Account

Use this set of instructions to create an external SoftLayer account that is
used:
- To order new devices
- To sign into control.softlayer.com

Note: You must be logged in to the SoftLayer VPN before proceeding

1. Go to https://internal.softlayer.com/
2. Login with your:
    - Internal SoftLayer development user name
    - Internal SoftLayer user credentials
    - Symantec VIP token from your mobile device
3. On the top right of the home page, search for 720429 in
"Customer - Account Id"
4. Click the company hyperlink for
"SoftLayer Internal - OpenStack Site Reliability Team"
or
"SoftLayer Internal - Compute Rch1"
5. In the "Account Users" section in the center column, find Theresa Backlund
6. Click the "control" link that is to the right of Theresa Backlund's name
7. Enter your Symantec VIP token and click "Log me in"
8. Select "Account" -> "Users"
9. Click "Add User" in the top right hand corner
10. Create your user and give yourself necessary privileges, permissions, etc.
Most users have been added using the syntax ``<name>-sl``.  For example,
`michaelwurtz-sl`.
11. Under the VPN column for your name, click on "VPN Access" and enable "SSL" access to your account
12. After you verify the user add permission to that new user.  Verify the status of the user;  it must have permissions as superuser.

## Finding The API Key For Your External SoftLayer Account

Your API key information is required for your workstation's RC file.
You must configure the RC file in order to utilize the
[OpenStack client](openstack_client.md) to run jumpgate CLI from your
workstation.

1. You can get to the control portal to find your API key in one of two ways:
    1. If signed into https://internal.softlayer.com/ and looking at the
"SoftLayer Internal - OpenStack Site Reliability Team" account:
        1. Find your external SoftLayer user name in the "Account Users"
section.
        1. Click on the "Control" link to the right of your external SoftLayer
        user name.
        1.  On the control panel that comes up, enter your Symantec VIP
        security code in the "Token" field
        1. Click "Log Me In."
    1. Go directly to https://control.softlayer.com/
        1. Sign in with your external SoftLayer user name and password
1. On the very top of the page click on your user name to bring up the
"Edit User Profile" page
1. Near the bottom of the "Edit User Profile" page you will find a section named
 "API Access Information."
1. The "API Username" is specified in the OS_USERNAME field in
your RC file
1. The 64 character Authentication key is specified in the
OS_PASSWORD field in your RC file
1. You will also find your "VPN Username" under your user information


## SoftLayer LDAP Groups
As part of onboarding by your manager you should be added to the appropriate
SoftLayer LDAP groups.  In addition, you will need to ask your squad lead or
manager to be added to any squad-specific LDAP groups.  The following LDAP
groups are specific to the compute-telemetry squad:
<li>compute-dev-telemetry<br>
See
[internal ticket 40539915](https://internal.softlayer.com/Ticket/ticketEdit/40539915) used to
create the AD for details.
