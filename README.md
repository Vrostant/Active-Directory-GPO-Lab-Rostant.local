# Active-Directory-GPO-Lab-Rostant.local

 GPOs Configured
1. Password Policy
Purpose: Enforce strong password requirements across all domain user accounts to reduce the risk of credential-based attacks.
Key Settings Configured:

Minimum password length
Password complexity requirements (uppercase, lowercase, numbers, symbols)
Maximum password age (forces regular rotation)
Minimum password age (prevents immediate reuse)
Password history (prevents reusing recent passwords)

Why It Matters:
Weak passwords are one of the most common attack vectors. Enforcing complexity and rotation policies significantly reduces the risk of unauthorized access through password guessing or credential stuffing.

2. Account Lockout Policy
Purpose: Protect domain accounts from brute force and password spray attacks by automatically locking accounts after a set number of failed login attempts.
Key Settings Configured:

Account lockout threshold (max failed attempts before lockout)
Account lockout duration (how long the account stays locked)
Reset lockout counter after (time window for failed attempt counting)

Why It Matters:

Without lockout policies, attackers can attempt thousands of password combinations undetected. This GPO adds a critical layer of defense by making brute force attacks impractical and alerting administrators through lockout event


3.  Desktop Wallpaper
Purpose: Deploy a standardized corporate desktop wallpaper to all domain-joined machines, reinforcing organizational identity and professionalism.
Key Settings Configured:

Wallpaper path (network share or local path)
Wallpaper style (Stretched, Centered, Tiled, etc.)
User configuration applied at logon

Why It Matters:
Beyond branding, a managed wallpaper can be used to display security notices, acceptable use policy reminders, or emergency contact information — all enforced consistently across the organization.

Drive Mapping
Purpose: Automatically map network drives for users upon logon, giving them seamless access to shared resources without manual configuration.
Key Settings Configured:

Drive letter assignment
Network path (UNC path to shared folder)
Action: Create / Update / Replace / Delete
Applied to: Authenticated Users
Link Enabled: Yes | Enforced: No

Why It Matters:
Automating drive mapping removes the need for end-user intervention, reduces help desk tickets, and ensures everyone has consistent access to the correct network resources based on their role or OU.
