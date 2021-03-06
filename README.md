
# Bloomreach Engagement

 Bloomreach Engagement data available directly inside you Zendesk sidebar. Click on the Engagement logo to access the full client.

  

### View:

* Customer Attributes

* Customer Segmentation

* Customer Aggregates

Or anything which can be accessed via the Bloomreach Engagement Customer API.
    
### Screenshots:

![sidebar_widget](./assets/screenshot-0.png)
![configuration](./assets/screenshot-1.png)

### installation

1) Input your engagement project id - this can be found in the project settings > project_token area of your Engagement project.
2) Input your engagement hostname. This is the domain of your Engagement admin interface - e.g. demo_project.exponea.com  
3) Input your engagement API hostname. This is available at project settings > api Base URL.
4) In Engagement, generate an API keypair for a private group. Turn these into a base 64 encoded token. An easy way to achieve this is to install nodejs, start the repl and paste: console.log(Buffer.from('<public_key>:<private_key>').toString("base64")) - put this value into the Engagement_token field
5) The final thing to do is to configure the fields you would like to display. This is configured in the Engagement_payload field as a JSON object in the form:

{
  "fields" : [
  {
	   "type": "segmentation attribute etc",
	   "id" : "the internal Engagement id of the field",
	   "label" : "what you want the name to be when display inside Zendesk"
	 },
	 {...},
	 {...}
   ]
} 

The exact values you require can be found by referring to the Bloomreach Engagement API Reference [here](https://documentation.bloomreach.com/engagement/reference/welcome)