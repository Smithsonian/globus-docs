# Creating Guest Collections for External Collaboration

This guide provides step-by-step instructions for Smithsonian researchers to create **Guest Collections** in Globus, enabling secure data sharing with external collaborators who don't have access to Smithsonian storage systems. Guest Collections act as a bridge, using the data owner's credentials to provide controlled access to specific directories.

### Smithsonian Globus Infrastructure

While many large-volume transfers involve the Hydra high-performance computing cluster, researchers can also leverage dedicated **Globus Data Transfer Nodes** located at:
- **Smithsonian Data Center** (includes Hydra and DAMS NAS storage)
- **STRI** (Smithsonian Tropical Research Institute)
- **SAO** (Smithsonian Astrophysical Observatory)

### Example Use Cases

Many Smithsonian researchers use Globus to share large datasets with external collaborators, particularly those requiring access to raw data files that are too large for email or cloud storage:

- A collaborative team at NMNH and STRI uses Globus to transfer pollen images generated on microscopes at NMNH to STRI, where they are analyzed and shared with external collaborators who provide taxonomic expertise by annotating the images according to their specialized knowledge of pollen identification.

- The Center for Conservation Genomics at NZCBI uses Globus to share genomic data externally with research partners around the world.

## Globus Access 

**TL;DR: Your Smithsonian account gives you access to Globus. To share data, you also need an account on the server where your data lives. When you create a Guest Collection, it uses YOUR server permissions to let external collaborators access your data - they don't need their own server accounts.**

| Access Type | What It Provides | Requirements |
|-------------|------------------|--------------|
| **Globus Web Application** | Interface to manage transfers, view activity, browse collections | Smithsonian network account  |
| **Creating Guest Collections** | Ability to share your data with external collaborators | Smithsonian network account + user account on the specific server hosting your data |
| **Accessing Shared Guest Collections** | Read/write data in collections shared with you | Globus account only (uses collection owner's server permissions) |

**Important Note:** While you can access the Globus web application interface with just your Smithsonian network account, you need user accounts on the specific storage systems (Hydra, STRI servers, etc.) to view and work with Collections containing data stored on those systems. Without the underlying storage access, Collections will appear as inaccessible in the Globus interface.

## Prerequisites

### For Data Owners (Sharing Data)
- [ ] Active Smithsonian network account 
- [ ] User account on the server hosting your data:
  - **Smithsonian Data Center users** (Hydra, DAMS NAS): Contact Hydra Sys Admins (SI-HPC@si.edu) for account creation
  - **STRI users**: Contact STRI Sys Admins (STRIhelp@si.edu) for Data Transfer Server account
- [ ] Data organized in a shareable directory structure (best practices outlined below)
- [ ] Understanding of your data's sensitivity (note: PII should not be transferred using Globus)

### For Data Recipients (Accessing Shared Data)
- [ ] Globus account (free institutional or personal account)
- [ ] Valid email address for sharing notifications

**Note**: Recipients do not need accounts on the underlying storage systems. The Guest Collection uses the data owner's permissions to provide access.

### Network Requirements
Once data is deposited in a Smithsonian-managed collection, all Globus actions can be managed from the web application (app.globus.org) without being required to be on the Smithsonian network or VPN.


## Data Sharing Workflow

<img src=images/sharing-1.png width="500">

*Access your institutional collection through the File Manager interface. Note the "Globus Tutorial Collection 1" dropdown and "Directory_To_Share" folder selection.*

### 1. Access Your Data Collection
- Log into Globus web application
- Navigate to File Manager (shown in left navigation)
- Select your institutional collection (e.g., "Globus Tutorial Collection 1")
- Browse to the directory you want to share

### 2. Create a Guest Collection

<img src=images/sharing-2.png width="500">

*Select the folder you want to share (blue highlighting shows selection) and click the Share button (red circle) from the action menu.*

- Select folder/directory to share using checkbox
- Click "Share" from the right-side action panel
- Choose "Add Guest Collection" from options

<img src=images/sharing-2-2.png width="500">

*Alternative pathway: From the collection overview, click 'Add Guest Collection' (red circle) to begin sharing process.*

### 3. Configure Collection Settings

<img src=images/sharing-4.png width="500">

*Configure your guest collection with descriptive information and security settings. Note the Display Name field ("DemoGuest") and Create Collection button.*

- **Directory Path**: Verify the correct subdirectory is selected
- **Display Name**: Choose a descriptive name (e.g., "DemoGuest" as shown)
- **Description**: Provide context for collaborators
- **Keywords**: Add searchable terms for discoverability
- Click "Create Collection" to establish shareable endpoint

### 4. Add Collaborators

<img src=images/sharing-4.png width="500">

*Access permission management from your newly created guest collection using the "Add Permissions — Share With" button (red circle).*

- Click "Add Permissions — Share With"
- **Choose Sharing Method:**
  - **User**: Share with specific individuals
  - **Group**: Share with predefined research groups
  - **All Users**: Share with any Globus user
  - **Public**: Allow anonymous access

![User permission configuration form](image-10.png)
*Configure basic user permissions for root directory access. Note the "user" radio button selection (red arrow), Email Notification checkbox (red arrow), and "Add Permission" button (red circle).*

- **Path**: Specify subdirectory access (defaults to root `/`)
- **User**: Enter collaborator's institutional identifier
- **Email Notification**: Enable to alert collaborators (recommended)
- **Message**: Customize invitation text ("Here's the data I was telling you about...")
- **Permissions:**
  - ☑️ **Read**: View and download files
  - ☐ **Write**: Upload and modify files

**Advanced Access Control:**

![Advanced path restriction configuration](image-11.png)
*Advanced: Restrict access to specific subdirectories by modifying the Path field. The red arrow shows "/subdir1/" limiting access to only that subdirectory.*

For enhanced security, you can limit access to specific subdirectories by changing the Path field from `/` to `/subdir1/` or other specific paths.

### 5. Assign Ongoing Roles (Optional)

![Roles management interface](image-12.png)
*Manage long-term collaboration through the Roles tab (red circle). Click "Assign New Role" (red circle) to add administrative responsibilities.*

For complex collaborations, assign specific roles:
- **Administrator**: Full collection management
- **Access Manager**: Manage permissions and sharing
- **Activity Manager**: Monitor transfers and usage
- **Activity Monitor**: View-only access to collection activity

![Role assignment interface](image-13.png)
*Assign specific roles to collaborators based on their responsibilities. The red arrow shows Access Manager selection, with "Add Role" button (red circle) to finalize assignment.*

### 6. Monitor and Maintain

![Active shared collection view](image-14.png)
*Your shared collection ("DemoGuest") is now accessible to collaborators with proper permissions. Monitor the file listing and manage ongoing access as needed.*

- Review active permissions regularly through the Permissions tab
- Update access as project needs change
- Revoke access when collaboration concludes
- Monitor activity for security and usage patterns
*Access your institutional collection through the File Manager interface. Note the "Globus Tutorial Collection 1" dropdown and "Directory_To_Share" folder selection.*


## Collaboration Best Practices

### Data Organization
- **Share Only What's Necessary**: Limit access to specific directories required for collaboration rather than providing broad access
- **Clear Directory Structure**: Use intuitive folder hierarchies like shown in the file listings
- **Comprehensive Documentation**: Include README files and metadata
- **Version Control**: Implement file naming conventions for updates
- **Access Boundaries**: Use path restrictions (see Image 7) to prevent unnecessary directory access

### Security Considerations

<img src=images/sharing-3.png width="500"> 

*Use descriptive but not revealing collection names for better security.*

- **Principle of Least Privilege**: Grant minimum required access
- **Regular Access Reviews**: Audit permissions quarterly through Roles management
- **Endpoint Security**: Ensure recipient systems meet security standards

### Communication

<img src=images/sharing-6.png width="500"> 

*Always enable "Send notification" and customize the message field with clear context about the shared data.*

- **Clear Sharing Notifications**: Customize email messages with context ("Here's the data I was telling you about...")
- **Usage Guidelines**: Provide collaborators with access instructions
- **Support Contacts**: Include help desk information for technical issues
- **Data Lifecycle**: Communicate retention and deletion policies

## Key Considerations for Data Sharers

### Before You Share
- **Verify Data Sensitivity**: Ensure no PII or other restricted data is included
- **Organize Thoughtfully**: Structure directories so collaborators can easily navigate
- **Test Access**: Verify the sharing setup works with a trusted colleague first
- **Document Clearly**: Include README files explaining data structure and usage

### Managing Ongoing Collaborations
- **Regular Access Reviews**: Periodically audit who has access to your collections
- **Clear Communication**: Keep collaborators informed about data updates or changes
- **Proper Closure**: Revoke access when projects end or collaborations conclude
- **Backup Coordination**: Ensure important collaborative data is properly preserved

### Using Globus for Internal Smithsonian Collaboration

While this guide focuses on external collaboration, these same tools and techniques can be used effectively for sharing data between Smithsonian departments, research units, and centers. Internal collaborations may have simplified account management since all parties already have Smithsonian network access, but the same principles of organized sharing, clear permissions, and proper access management apply.

## Support and Additional Resources

### Getting Help
- **SI-Globus@si.edu**: General Globus support and troubleshooting
- **SI-HPC@si.edu**: Hydra account creation and system-specific issues
- **STRIhelp@si.edu**: STRI Data Transfer Server account creation and support
- **Globus Documentation**: Comprehensive platform guides and tutorials

### Training Opportunities
- **Globus Webinar Series**: Regular platform updates and advanced features
- **Institutional Workshops**: Hands-on training for research teams
- **Documentation Resources**: Step-by-step guides and video tutorials
- **Peer Learning Groups**: Connect with other Smithsonian researchers

---

*For technical support with Globus collections and data access, contact SI-Globus@si.edu. For questions about account creation, contact the appropriate system administrators listed above.*