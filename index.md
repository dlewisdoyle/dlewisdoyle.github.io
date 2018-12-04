---
---


Quickstart: Installing ownCloud and Connecting to It as a Client
=================================================================
This Quickstart Guide describes the basic administration tasks for installing and using ownCloud, the open source file synchronization and sharing solution for servers that you control. ownCloud includes the ownCloud server, which runs on Linux, client applications for Microsoft Windows, Mac OS X and Linux, and mobile clients for the Android and Apple iOS operating systems.  


Installing and Configuring an ownCloud Server 
---------------------------------------------

1. Confirm that you meet the General Recommendations for System Requirements:   
   * Operating system: Linux
   * Web server: Apache 2.4
   * Database: MySQL/MariaDB with InnoDB storage engine
   * PHP 5.6+
   * For the complete list of supported platforms and options, see [System Requirements](https://doc.owncloud.com/server/10.0/admin_manual/installation/system_requirements.html/"Title").

2. Ensure you have Command Line *and* Cron Access. To perform all administrative tasks reliably, (such as repairs, upgrades, background jobs, and long-running operations), you will need both access types.
   * For more information, see [Deployment Recommendations](https://doc.owncloud.com/server/10.0/admin_manual/installation/deployment_recommendations.html/"Title").

3. Install ownCloud on Linux from our [Open Build Service packages](https://doc.owncloud.com/server/10.0/admin_manual/installation/linux_installation.html/"Title"). 
   * If there are no packages for your Linux distribution or you prefer installing from the source tarball, see [Manual Linux Installation](https://doc.owncloud.com/server/10.0/admin_manual/installation/source_installation.html/"Title").

4. Run the Installation Wizard:
   * Point your web browser to http://localhost/owncloud.
   * Enter your desired administrator’s username and password.
   * Click “Finish Setup”.
   * For more information, see [Installation Wizard](https://doc.owncloud.com/server/10.0/admin_manual/installation/installation_wizard.html/"Title").

5. Follow guidelines in [Configuration Notes & Tips](https://doc.owncloud.com/server/10.0/admin_manual/installation/configuration_notes_and_tips.html/"Title").
   * ownCloud recommends the use of **PHP 7.2** in new installations. Sites using a version earlier than PHP 7.2 are strongly encouraged to migrate to PHP 7.2.


Enabling Users to Connect to the ownCloud Server
------------------------------------------------
1. In your config.php file, under the trusted_domains setting, add the server IP address to which users can point their browsers.

A typical configuration looks like this:
       
    'trusted_domains' => [
       0 => 'localhost',
       1 => 'server1.example.com',
       2 => '192.168.1.50',
    ],
    
2. In the Apache server, change the port to 8080.

   * For details, see [How to change the port ownCloud is using](https://central.owncloud.org/t/how-to-change-the-port-owncloud-is-using/834.html/"Title").


Creating a User Account
-----------------------
1. On the left sidebar of the User Management Page, click "users".
2. Enter the new user’s Login Name, initial Password, and email address.
3. Click "Create".

*Note:* The local user creation flow requires both a username *and* an email address. Users receive email notification with an activation link which provides a more efficient, secure experience. Administrators who want to set the initial password can select the “Set a password for new users” option on the bottom left settings cog.


Connecting to the ownCloud Server from a Desktop or Mobile Client
-----------------------------------------------------------------
The ownCloud Desktop Sync Client enables you to connect to *your own* private ownCloud Server. Changes you make to the files on one computer update those files on your other devices. ownCloud makes it possible to have your latest files with you wherever you are.

**Desktop System Requirements**
 
   * Desktop client version 2.0 or higher
   * Windows 7+
   * Mac OS X 10.7+ (64-bit only)
   * CentOS 6 & 7 (64-bit only)
   * Debian 8.0 & 9.0
   * Fedora 25 & 26 & 27
   * Ubuntu 16.04 & 17.04 & 17.10
   * openSUSE Leap 42.2 & 42.3

Download your [ownCloud Desktop Client for MacOS, Windows, or Linux](https://owncloud.org/download/#owncloud-desktop-client.html/"Title").

For installation and usage guidelines, see the [ownCloud Desktop Client Manual](https://doc.owncloud.com/desktop/latest.html/"Title").

To learn what's new in version 10.0.10, how to configure external storage, how files and synchronization work, and more, see the [User Manual](https://doc.owncloud.org/server/latest/user_manual/contents.html/"Title").

To learn how to connect Linux, Mac OS X, Windows, and mobile devices to your ownCloud server via WebDAV, see [Accessing ownCloud Files Using WebDAV](https://doc.owncloud.org/server/latest/user_manual/files/access_webdav.html?highlight=mobile.html/"Title").

You can view and manage your desktop and mobile activity in [Personal Browser and Device Settings](https://doc.owncloud.org/server/latest/user_manual/session_management.html/"Title").

For updates, blogs, developer forums, and more, see [ownCloud's Newsroom](https://owncloud.com/newsroom.html/"Title").## Welcome to GitHub Pages
