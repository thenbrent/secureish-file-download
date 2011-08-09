=== Secure(ish) File Download ===
Contributors: thenbrent, anthonycole
Tags: download, file download, download counter, picture download, file types, shortcode
Requires at least: 3.1
Tested up to: 3.2.1
Stable tag: 0.1

Use [shortcodes](http://codex.wordpress.org/Shortcode) to protect the URI of your file downloads and require a user to be logged in.

== Description ==

Information wants to be free. On the one hand bandwidth wants to be expensive. Secure(ish) File Download prevents unauthorised downloading of files on your website.

There is no interface, simply use [shortcodes](http://codex.wordpress.org/Shortcode) to offer a range of file downloads on your site.

= Examples =

The simplest shortcode possible is to specify only the `file` attribute:

`[secure_download file="http://example.com/file.zip"/]`

This will output a *Download* link for which a user must be logged in to access.

The value of the `file` attribute can be either an absolute path on your file system or a URL to a file.

If you would like the file to begin download automatically, add an `id` and `auto_download` attribute. The `auto_download` attribute should be a time is seconds longer than 0 that specifies the period to wait before commencing the download.

`[secure_download id="ego" auto_download="3000" file="http://example.com/file.zip" ]The file should begin downloading automatically after 3 seconds. If it does not, click here.[/secure_download]`

To remove the authentication requirement, you can set the `login_required` attribute to `false`. 

`[secure_download login_required="false" file="http://example.com/file.zip"]Download via hashed URL[/secure_download]`

This will make the download accessible by all users.

To obscure the filename in the download URL, set the `hash_permalink` attribute to `"true"`. 

`[secure_download hash_permalink="true" file="http://example.com/file.zip"]Download via hashed URL[/secure_download]`

This will change the download URL from `http://example.com/secure-download/file.zip` to something like `http://example.com/secure-download/97386dcaf6711efe4d3af808f5dc09ce`. As the hash does not change over time, this has arguable value in securing your files.

== Installation ==

1. Unzip and upload `/secure-file-download/` to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Add a [secure_download] shortcode to your pages or posts (see example shortcodes for details)


== Changelog ==

= 0.1 =
First version.
