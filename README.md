# Salesforce
Notes for salesforce-Admin

User Management:

1) **Add new user:**

To add users:

1. From Setup, enter Users in the Quick Find box, then select Users.
2. Click New User to add a single user or click Add Multiple Users to add up to 10 users at a time.
3. Enter each user's name, email address, and a unique username in the form of an email address. By default, the username is the same as the email
address, but you can overwrite this.
4. Select the user license you want to associate with the users you create (the license determines which profiles are available for each user).
5. Select a profile.
6. Select Generate passwords and notify user via email to email a login name and temporary password to each new user.
7. Click Save.

2) **Control What Your Users Can Access:**

- Describe the difference between object and field level security
- Describe how to set org–wide default sharing settings

- **Organization–wide defaults** specify the default level of access that users have to each others' records. You use organization–wide sharing settings to lock down your data to the most restrictive level, and then use the other sharing tools to selectively give access to other users. For example, you can give all employees access to an object called Candidate to allow anyone to add a candidate to the database. But you can restrict access to Positions so that anyone can see the jobs available but only the employees with the proper permissions can edit them.
- **Role hierarchies** open up access to those higher in the hierarchy so they inherit access to all records owned by users below them in the hierarchy. Role hierarchies don't have to match your organization chart exactly. Instead, each role in the hierarchy represents a level of data access that a user or group of users needs. For example, you can restrict access to Candidates by setting the organization–wide default to Private, but allow recruiters to view and edit the candidate records that they own. Recruiters can't see candidate records they don't own because recruiters are all at the same level in the role hierarchy. However, hiring managers can be given read/write access to all candidate records because they are at a higher level in the role hierarchy than recruiters.
- **Sharing rules** enable you to make automatic exceptions to organization–wide defaults for particular groups of users, to give them access to records they don't own or can't normally see. Sharing rules, like role hierarchies, are only used to give more users access to records—they can't be stricter than your organization–wide default settings. For example, you can allow all employees to view Positions, but use sharing rules to grant full editing access to employees in a role or group called Hiring Managers.
- **Manual sharing** allows owners of particular records to share them with other users. Although manual sharing isn't automated like organization–wide sharing settings, role hierarchies, or sharing rules, it can be useful in some situations, for example, if a recruiter going on vacation needs to temporarily assign ownership of a job application to another employee.


**Organization-Wide Sharing Defaults**

Now that you've learned more about record-level security, let's focus on organization-wide defaults. These are the defaults that specify the baseline level
of access that users have to records that they don't own. Configure your organization-wide defaults for what the most restricted user is allowed to access.
Then use other record-level security and sharing tools (role hierarchies, sharing rules, and manual sharing) to open up the data to other users who need
to access it.
You can specify the default level of access to records for each type of standard or custom object. You can never use organization-wide defaults to grant
users more access than they have through their object permission.
You can determine the organization-wide defaults you need for your app by answering the following questions for each object.

1. Who is the most restricted user of this object?
2. Is there ever going to be an instance of this object that this user shouldn't be allowed to see?
3. Is there ever going to be an instance of this object that this user shouldn't be allowed to edit?
