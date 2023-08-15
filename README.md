# Related Ticket Manager

The **Related Ticket Manager** app was developed to help Zendesk agents to find and relate tickets based on key phrases. Once a list of matching tickets is returned, the ticket being worked on can be easily linked to them (as a problem or as an incident) through the app interface.

## Minimum requirements

- **Zendesk Support Professional** or above

## Key features

- Multiple terms can be searched by separating terms by a comma.
- Commas will always be interpreted as an "OR" operator.
  - Example:
    > - **Search terms:** password, order
    > - **Results:** both tickets containing **password** OR **order**
- Spaces will always be interpreted as an "AND" operator.
- Testing again
  - Example:
    > - **Search terms:** reset password
    > - **Results:** both tickets containing **reset** AND **password**
- Advanced search operators can also be used.
  - Example:
    > - **Search terms:** ticket_type:problem created>2020-08-12
    > - **Results:** only problem tickets created after **2020-08-12**
  - The list of advanced operators can be found at https://support.zendesk.com/hc/en-us/articles/203663226#topic_crj_yev_uc.
- Multiple terms can be used even if using advanced search methods.
  - Example:
    > - **Search terms:** ticket_type:problem reset, ticket_type:incident password
    > - **Results:** both **problem tickets** containing the _reset_ keyword OR **incident tickets** containing the _password_ keyword.
- Results are paginated so the app will always run smoothly regardless of the number of tickets returned. The page size can be defined when installing the app.
- The ticket being worked on can be linked to an already open problem and become an incident.
- Any ticket (if not a problem) can become a problem ticket and have incidents attached to them directly from the app screen.
- Different ticket types are displayed with different colours to improve the user experience.
- The app will automatically search for key phrases as soon as the agent opens a ticket screen if a custom ticket field ID with key phrases is provided during the app installation.

## How to install

- Download the latest version of this app.
- Upload the file above to your Zendesk Support as a private app by following [these instructions](https://develop.zendesk.com/hc/en-us/articles/360001069347-Uploading-and-installing-a-private-app).
- Enter the requested app settings.
- Click Install.

Once all the steps above are done, your app will be available on the sidebar of any ticket screen.

## Download

- Latest version (v1.1.0): http://goto.zendesk.com/related-ticket-manager

## Github

- Github repository: https://github.com/zendesk/related_ticket_manager

## App screenshot

![](https://user-images.githubusercontent.com/48917373/90786057-082c2180-e2fb-11ea-8d9f-560af86ecf1a.gif)

## Author

This app has been developed and maintained by **Marcelo De Bortoli** (EMEA Solution Developer).

## Credits

- [Vue.js](https://vuejs.org/)
- [Vuetify](https://vuetifyjs.com/en/)
- [Font Awesome](https://fontawesome.com/)
- [Zendesk Apps Framework](https://developer.zendesk.com/apps/docs/developer-guide/getting_started)

## Changelog

### v1.1.0 (2020-08-21)

- Added ticket creation date
- General refactoring

### v1.0.0 (2020-08-19)

First version released.
