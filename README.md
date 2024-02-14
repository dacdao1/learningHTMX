What is HTMX and the background information on web app development.

web 1.0:
The goods: MPA and Hypermedia. The bads: limited hypermedia control. Difficult to build complex interfaces. User interaction with the website was difficult.
EXAMPLE website of web 1.0 - https://jkhub.org/mapping/richdiesal/richdiesal.htm

web 2.0:
The goods: one page for front end. DOM is managed with JavaScript. APIs data are returned to the page. The beginning of different front end frameworks, React, Vue, Angular, Svelte. The bads: heavy JavaScript framework, most of the library are stored in clients. Not a lot of hypermedia controls.

HTMX:
It is a hypermedia oriented library. Bridge between web 1.0 and web 2.0. Hypermedia native controls. Consume APIs and update the DOM natively.
SPAs uses a JavaScript model architecture (the UI updating the DOM and the DOM updating the UI). HTMX uses native hypermedia architecture.

When to use HTMX?
No need for ui model or routing. Not a lot of user-interactivity, frontend framework can display the data and HTMX can fetch the data. DON'T use HTMX if there is a lot of complex interaction between the user and the application or application that makes alot of state changes without interacting with the server.

Hypermedia API:
API based on Hypermedia as the Engine of application state (HATEOAS). Provide more then just data, also include hypermedia like links.

HOW TO USE HTMX:

To use any of the RESTapi commands, use hx-{get,post, put, patch, delete} on the action attribute of the html file. Then use hx-target, to target the element(div, h1, p, etc...) that you want the data to display.

Without the hx-target attribute, the data will load into the parent component that use the hx- call to the server.

- hx-trigger will use different build in event to trigger the api call
- hx-trigger can use the keyword, once, to only trigger that particular event once.
- hx-trigger can use the keyword, delay:{enter the amount of time}, to trigger the event with that delay time.
- hx-trigger can use the keyword, from:#{id of the atrribute the action is coming from}, to add the data to the current attribute. PLEASE look at the code within triggers.html for an example.
- hx-trigger can use the keyword, click[{javascript code here}], and the code will execute the JavaScript code within the bracket.
