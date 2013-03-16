=== Better Notifications for WordPress (beta) ===
Contributors: jackmcconnell, peterrocker
Tags: notifications, email, roles, custom
Requires at least: 3.5
Tested up to: 3.5
Stable tag: 0.1b

Send customisable HTML emails to user roles for different WordPress notifications. 

== Description ==

Better Notifications for WordPress (beta) allows you to choose which WordPress email notifications are sent to which user roles (including custom roles) and allows you to customise those emails using all the available information WordPress provides for that notification using simple shortcodes. Emails are sent using the built in wp_mail() but can be sent using SMTP using an appropriate 3rd party plugin (we recommend WP-Mail-SMTP).

For example: 
You want Editors to be alerted via email when a new post is published and you'd like that email to be in HTML so you can include your branding along with the author's display name and post time - with this plugin, that's easy. 

Notifications that you can use are: 

* New category
* New post published / post updated
* New comment (and it's corresponding status)
* New user registration
* New trackback
* New pingback
* Lost password reset

If you'd like to see a notification in the list above, please get in touch via plugins [at] voltronik.co.uk and we'll see what we can do to add it.
Having problems? Please let us know via this plugin's forum so we can address them and let it act as a source of information for future reference and other users.

Like this plugin? Please leave us a great review! 
Don't think the plugin is worthy of 5 stars? Let us know on the forum or drop us a line at plugins [at] voltronik.co.uk and we'll try and help. 



== Installation ==

1. Upload the 'bnfw' plugin folder to the '/wp-content/plugins/' directory or download it via your WordPress installation.
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Use the new 'Notifications' Menu item in the sidebar to configure the plugin.
4. (Optional) Install a plugin to use SMTP instead of wp_mail(). We recommend WP-Mail-SMTP.
5. Test by creating an update for the defined notification (e.g. create a new post if the new posts notification has been set-up).
6. Depending on you requirements, you may need to switch on or off some of the default WordPress settings. Please see the FAQ section for more information.



== Frequently Asked Questions ==

= How do I set-up WordPress to work with this plugin correctly? =

This will very much depend on what notifications you're using the plugin for. Out-of-the-box, this plugin works very well but there are a few tweaks that you will need to ensure 100% compatibility. All the below points refer to our plugin: 

* If you want to use the new comment notifications in BNFW, you need to switch off 'Email me whenever anyone posts a comment' and 'A comment is held for moderation' under Settings > Discussion. It's ok if you don't do this but you might receive WordPress's own email notifications along with the ones you configure using BNFW too. It also goes without saying that you need to enable comments for your posts if you want the email notifications to come through. 

* If you want to use the trackback / pingback BNFW notification, then you need to switch on 'Attempt to notify any blogs linked to from the article' and 'Allow link notifications from other blogs (pingbacks and trackbacks)' under Settings > Discussion.

= Configured Emails aren't coming through! =

Check your settings to make sure all is as it should be, then check your spam folder. Gmail and certain hosts can mark messages from new websites (or IP addresses) as spam so it's worth checking and possibly creating a filter to ensure this doesn't happen in the future.

= The email previews aren't showing the contents of the shortcodes! =

This is by design. In order to show the contents, the plugin would have to retrieve information for a specific event and it's hard to tell which one you'd like to use or if there's any information in the database. The previews will show your HTML rendering, however. 

= Some of my shortcodes aren't working! =

It's possible you're inserting a shortcode into an email for a notification that cannot use it. WordPress imposes certain limitations on information outputted for particular notifications. For example: the 'New Category' email notification cannot use any of the author or time shortcodes as WordPress only stores (and subsequently returns) the category name, category slug and category description. It's also worth checking the spelling and hyphens in any shortcodes as well as if they are wrapped in square brackets '[]'.
 


== Screenshots ==

1. The notifications and roles settings. Set which roles you'd like to receive emails for notifications from here.
2. The email templates screen. Customise your emails using HTML and shortcodes here.



== Changelog ==

= 0.1 beta =
* Initial version of the plugin.
* Settings page for configuring notification types for roles.
* Email Templates page for customising emails using HTML and shortcodes.