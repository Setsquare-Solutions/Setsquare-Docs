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

* `[FormDisplay]` - outputs a form. Allowed values:
    * `id=""`       - the ID of the form to output

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
    * `navigation=""`   - **true** or **false**, display buttons to navigate to next/previous month
    * `events=""`       - **true** or **false**, include events
    * `meetings=""`     - **true** or **false**, include meetings
    * `small=""`        - **true** or **false**, use a design to accommodate smaller devices or spaces on the website.
    
    Small calendars will only show the date number, with a coloured highlight if events take place on that date.
    <br>The date can be clicked to pop-up a window with more details.
    <br>Regular calendars include a list of events below the date number.

---

* `[NewsletterDisplay]` - outputs a collection of newsletters or a single one:
    * `single=""`             - **true** or **false**, display a single newsletter
    * `id=""`                 - the id number of the single newsletter to display, this can be found in the [newsletters section](/newsletters/list.md)
    * `include-future=""`     - **true** or **false**, whether to allow newsletters from dates in the future to be displayed
    * `include-latest=""`     - **true** or **false**, whether to include the latest upto date newsletter, this can be useful to ommit if the latest newsletter is display separately to the list of past newsletters
    * `show-empty-message=""` - **true** or **false**, whether to display a message that no newsletters exist, if none could be found matching the other parameters
    * `items=""`              - the number of newsletters to display per page, if more than this number exists then page numbers will be displayed for navigation
    * `limit=""`              - the total number of newsletters to display overall

---

* `[CheckoutDisplay]` - outputs a Stripe checkout form, allowing a visitor to enter an amount and reference number to pay by card.