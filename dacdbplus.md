# DACdb Plus

DACdb Plus is a robust WordPress plugin, giving clubs and districts the ability to display lots of DACdb content on their WordPress website.

## Installation

1. Extract the latest release archive to your local folder, then upload it to your WordPress plugins dashboard.
2. From your installed plugins list, find **DACdb Plus** and click *"Activate."*
3. Once activated, click *"Settings"* and enter your Account/District number and Club/Chapter/Region number.

> :bulb: **Tip:** Your district and club id numbers can be easily found by logging in to [DACdb](https://dacdb.com/) and clicking the *"My Data"* tab!

4. Select your subscription type from the *"System"* dropdown list.
5. You may now browse and adjust display settings, or scroll to the bottom and click *"Save Changes."*

---

## How To Display Your Organization's Data

To display data from DACdb on your website, you must add small blocks of text called a **[shortcode](https://wordpress.com/support/wordpress-editor/blocks/shortcode-block/ "Click to learn more about WordPress shortcodes.")** to fields in the WordPress editor. To begin, we'll create a test page to experiment with short codes.

1. From the WordPress dashboard, click *"Pages"* from the left-hand column.
2. Click *"Add New"* button at the top of the page next to **"Pages."**
3. Click on *"Add Title"* and type `Club Information` then press enter.
4. Press the `/` key on your keyboard, then click *"[/] Shortcode"* from the dropdown list.
5. Click inside the field that says *"Write shortcode here..."* and type (or copy and paste) this entire block:

    ```text
    [dacdb_plus show="meeting_info"]
    ```

6. Click the *"UPDATE"* button in the top right hand corner.
7. In the bottom left corner, you'll see a confirmation that says **"Page updated."** Click the *"View Page"* link next to that to view your page.

---

## Supported Shortcodes

|Name|Shortcode|Notes|
|---|---|---|
|areas|`[dacdb_plus show="areas"]`|Districts only.|
|birthdays|`[dacdb_plus show="birthdays"]`||
|calendar|`[dacdb_plus show="calendar"]`||
|club_meetings|`[dacdb_plus show="club_meetings"]`|Clubs only.|
|club_presidents|`[dacdb_plus show="club_presidents"]`|Clubs only.|
|clubleaders|`[dacdb_plus show="clubleaders"]`|Clubs only.|
|cog|`[dacdb_plus show="cog"]`|Districts only.|
|committees|`[dacdb_plus show="committees"]`||
|committee|`[dacdb_plus show="committee"]`||
|committee_leaders|`[dacdb_plus show="committee_leaders"]`||
|dcc|`[dacdb_plus show="dcc"]`|Districts only.|
|d_leaders|`[dacdb_plus show="d_leaders"]`|Districts only.|
|documents|`[dacdb_plus show="documents"]`||
|events|`[dacdb_plus show="events"]`||
|~~JSONclubleaders~~|~~`[dacdb_plus show="JSONclubleaders"]`~~||
|leaders|`[dacdb_plus show="leaders"]`|Clubs only.|
|map|`[dacdb_plus show="map"]`|Districts only. You will need to enter a [Google Maps API Key](https://developers.google.com/maps/documentation/javascript/get-api-key "Click to get an API key for your site. A free Google Developer account is required.") on the settings dashboard in order to render a map.|
|meeting_info|`[dacdb_plus show="meeting_info"]`||
|members|`[dacdb_plus show="members"]`|Clubs only.|
|newsletter|`[dacdb_plus show="newsletter"]`||
|speakers|`[dacdb_plus show="speakers"]`||
|sponsors|`[dacdb_plus show="sponsors"]`||
|stories|`[dacdb_plus show="stories"]`||
|wcm|`[dacdb_plus show="wcm"]`|Districts only.|