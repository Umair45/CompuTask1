This is my first Drupal theme and developed for Drupal version 8.x .It is responsive theme without using any framework. Tested with the latest version of Firefox, Google chrome, Safari and IE11.

I followed the instructions of Drupal theming from:

http://watch-learn.com/series/drupal-8-theming

## **Drupal compatibility:**

This theme is compatible with Drupal 8.x.x

Installation: Simply extract, copy and paste to /themes directory. Enable it from the admin/appearance/

## **Installation:**

Assuming you have already installed the Drupal 8.x in your machine. Now follow the following steps:

1. Copy and paste the extracted opencharity folder to /themes.
2. From admin/appearance enable and set default the theme.
3. Now add new content type from admin/structure. I have added three content types for three different regions (Banner, Next Event, Services, Our Mission, Our Members, Our Mission Items and Blog). I have added some new required fields in these content types.
4. Add some content for various regions.
5. Now add different views for Banner, Blog, Next Event, Our Members, Our Mission, Our Mission Items and Services from admin/structure/views.
6. Then, you would have to go to admin/structure/blocks to add the required blocks to specific regions. You will get the newly created views title in the block list below. Just select the region from select box and click save blocks.
7. Add new block for Logo, Navigation, Banner, Next Event, Services, Our Members, Our Mission, Our Mission Items and Blog regions.
8. From admin/structure/menu &gt; Main menu you can add menu items.

## **Demo Link:**

For Demo please visit  [http://dev-ocharity.pantheonsite.io/](http://dev-ocharity.pantheonsite.io/)

Admin login Page [http://dev-ocharity.pantheonsite.io/user/login](http://dev-ocharity.pantheonsite.io/user/login)

Admin page [http://dev-ocharity.pantheonsite.io/admin](http://dev-ocharity.pantheonsite.io/admin)

# Theme Architecture

Created Different content types for every section on front page and then created template files for each of them to override their default html with my own custom html. Following is the list of content types and their fields and associated twig template files.

**Content Types**

There is a default Title field in all content types.

**Banner:**

Content for Hero banner section on front page.

[Fields: Banner Detail (text long)] Title is wrapped in H2 tag in the banner view.

views-view-unformatted--banner.html.twig

**Next Event:**

For next Event section just to go in Next event section

[Fields: Event Detail (text long), event start date (date), button link (link)

HTML changes is added in these files

views-view-unformatted--next\_event.html.twig

views-view-fields--next\_event.html.twig

**Services:**

To show items in Get Involved section. [Fields: Body (text long), Button Link (Link), Img (Image), Title (text)

Image is wrapped in a div with class &quot;wrap&quot; and button link is wrapped in a div with class btn from services view.

views-view-unformatted--services.html.twig

**Our Mission:**

Our Mission Title and Heading. [Fields: Mission Detail (text long)

Our mission title is wrapped into H2 in our\_mission view

**Our Mission Items:**

Add mission items. [Fields: body (text), icons(image)

Mission icon is wrapped in a div with class &quot;img-wrapper&quot; and title is wrapped into H3 in mission\_items view.

views-view-unformatted--mission\_items.html.twig

**Our Members:**

Our Members slides contents on front page. [Fields: member logo (image), you&#39;ll find this in admin =&gt; Structure =&gt; Content Types =&gt; Respective Content Type]

We use swiper slider to make slider and all html changes in this file. You can find this in themes =&gt; opencharity =&gt; templates

views-view-unformatted--members.html.twig

**Blog** :

Blogs posts shown on front page in blogs section. [Fields: body (text long), date (date)

Blog title is wrapped into H3 and date is wrapped into span in blogs view.

views-view-unformatted--blogs.html.twig

**Other Templates:**

**block.html.twig**

I have removed some unnecessary html from this file.

**block--system-branding-block.html.twig**

I have changed some HTML and add a logo class in site branding.

**html.html.twig**

I have included fonts and added some html (noscript tag, old browser error)  in this file which loads on all pages of the site.

**menu.html.twig**

I have added menu class in this file.

**page.html.twig**

I have included header and footer and add default HTML for all pages of the site.

**page--front.html.twig**

This is our Home page and I have included header, footer and all regions of our home page.

**Known Issues** :

1. This is my first time to use Drupal and the theme is developed for Drupal 8.x versions, the reason for choosing this version is I am not familiar with Drupal 7 at all. However, I had studies few articles on Drupal 8 theming in the past and I had little idea on how to proceed with Drupal 8 theming therefore I opted for Drupal 8.

1. Font family does not match the provided PSD because used fonts are not free.
2. Footer is static html from template.
3. After login Administrative links do not work you have to manually open admin page.
