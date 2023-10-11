# Shortcodes

Shortcodes are small pieces of special text that can be inserted into a page to perform more complex functions, that you may not be able to create yourself through the content editor. 

Shortcodes follow the format of a command word enclosed in square brackets with additional information passed using quotation marks. For example:

    [MyCustomCommand parameter1="my custom value" parameter2="another custom value"]

The simplest real example would be the shortcode to display a form. FormDisplay tells the system it needs to output a form, id=”x” tells it which form to output.

    [FormDisplay id="1"]

Shortcodes have to be created individually so you aren’t able to pass any information you like. A list of currently created shortcodes and what can be passed to them is below.

* `[CommitteeDisplay]` - outputs a link or collection of links to a committee page. Allowed values:
    * `name=""`     - the name of a single committee
	* `category=""` - the name of a group of committees
    * `order=""`    - **asc** or **desc**, should these committees be listed alphabetically or reverse alphabetically 

---

* `[CouncillorDisplay]` - outputs a single or collection of councillor profiles. Allowed values:
    * `ward=""`     - the name of a ward
    * `party=""`    - the name of a party
    * `name=""`     - the name of a councillor
    * `order=""`    - **asc** or **desc**, should these councillors be listed alphabetically or reverse alphabetically

---

* `[EmployeeDisplay]` - identical to CouncillorDisplay except that it replaces the word **Ward** on their profile with **Position**.

---

* `[FormDisplay]` - outputs a form. Allowed values:
    * `id=""`       - the ID of the form to output

---

* `[GalleryDisplay]` - outputs a selection of images that have been uploaded to the CMS. Allow values:
    * `folder=""`   - the path to a folder in the file manager. Multiple can be supplied, add a number to the end. (folder1="", folder2="")
    * `image=""`    - the path to a single image in the file manager. Multiple can be supplied, add a number to the end. (image1="", image2="")
    * `sort=""`     - **asc** or **desc**, should the images be displayed alphabetically or reverse alphabetically
    * `id=""`       - a unique id for the galley. Allows images to be shown full screen with arrows to navigate through each
    * `captions=""` - a comma separated list of captions for each image. Captions will be added to the images in the order they appear in the gallery. Enter no value to skip a caption. e.g. (caption 1,caption 2,,caption 4)

---

* `[MapDisplay]` - outputs a google map that can also have a marker on it. Allowed values:
    * `lat=""`      - the latitude of the point you want to focus on or display a marker. This can be found by clicking any point on Google Maps. It appears at the bottom of the screen
    * `lng=""`      - the longitude of the point you want to focus on or display a marker. This can be found by clicking any point on Google Maps. It appears at the bottom of the screen
    * `zoom=""`     - a numerical value to set how zoomed in the map is. 0 is the most zoomed, 12 is about average
    * `marker=""`   - **true** or **false**, do you want a red marker to be added to this point on the map

---

* `[SliderDisplay]` - outputs a slider similar to the carousels into the page. Allowed values:
    * `images=""`       - a comma separated list of paths to images uploaded to the CMS
    * `captions=""`     - a comma separated list of captions in the same order as the supplied images
    * `fits=""`         - **cover** or **contain**, cover will crop the image to fit the same height as the tallest, contain will show the whole image but can lead to white space around the edges
    * `wrap=""`         - **true** or **false**, true will loop the slider to the beginning once the end is reached
    * `interval=""`     - a number in milliseconds for how fast to loop through automatically. e.g. 1000 is 1 second
    * `aspect-ratio=""` - **portrait**, **landscape** or **square**, how the images will be cropped
    * `controls=""`     - **true** or **false**, if the arrows should be shown
    * `indicators=""`   - **true** or **false**, if the dots along the bottom showing how many slides should be shown

---

* `[CalendarDisplay]` - outputs a calendar of meetings or events. Allowed values:
    * `navigation=""`   - **true** or **false**,, display buttons to navigate to next/previous month
    * `events=""`       - **true** or **false**,, include events
    * `meetings=""`     - **true** or **false**,, include meetings
    * `id=""`           - add a unique ID for the calendar, only needs to be set if more than one calendar is added to a page
    * `small=""`        - **true** or **false**, use a design to accommodate smaller devices or spaces on the website. 
    
    Small calendars will only show the date number, with a coloured highlight if events take place on that date.
    <br>The date can be clicked to pop-up a window with more details.
    <br>Regular calendars include a list of events below the date number.