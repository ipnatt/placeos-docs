---
title: PlaceOS Event Mailer Driver
description: Access this System's Event and Bookings data, via the Mailer Driver
---

# PlaceOS Event Mailer Driver
* Type: Service Driver
* Dependencies: PlaceOS Driver
* Source: https://github.com/PlaceOS/drivers/blob/master/drivers/place/event_mailer.cr
## Functions

* Subscribes to events
* Sends emails to attendees for events

## Settings

| Key | Type | Default value | Description |
| --- | --- | --- | --- |
|`zone_ids_to_target`|  | ["zone-id-here"] | 
|`module_to_target`|  | "Bookings_1" | 
|`module_status_to_scrape`| String | "bookings" | 
|`event_filter`| String | "occurs_today" |
|`email_template_group`| String | "events" | 
|`email_template`| String | "welcome" | 
|`send_network_credentials` | Boolean | false | 
|`network_password_length`| Int32 | DEFAULT_PASSWORD_LENGTH | 
|`network_password_exclude`| String | DEFAULT_PASSWORD_EXCLUDE | 
|`network_password_minimum_lowercase` | Int32  | DEFAULT_PASSWORD_MINIMUM_LOWERCASE | 
|`network_password_minimum_uppercase` | Int32 | DEFAULT_PASSWORD_MINIMUM_UPPERCASE | 
|`network_password_minimum_numbers` | Int32  | DEFAULT_PASSWORD_MINIMUM_NUMBERS | 
|`network_password_minimum_symbols`| Int32 | DEFAULT_PASSWORD_MINIMUM_SYMBOLS |
|`network_group_ids`| String | [] of String
| `date_time_format` | String | "%c"
| `time_format` | String | "%l:%M%p"
| `date_format` | String | "%A, %-d %B"
| `debug` | Boolean | false
| `target_zones` |  | [] of String
| `target_module` |String | "Bookings_1"
| `target_status` |String | "bookings"
| `event_filter` |String | "occurs_today"
| `email_template_group` |String | "events"
| `email_template` | String | "welcome"
| `send_network_credentials` | Boolean | "false"
| `network_group_ids` | | [] of String
| `events` | | {} of String

## Commands

### `subscribe_to_all_modules`
Subscribe to the targeted state of all matching modules and update our state when they change

#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
|  | 
#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```

### `list_target_systems`

#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
|  | 
#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```

### `list_systems_in_zone`

#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
| zone_id | | String
#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```

### `inspect_event_store`

#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
|  | 
#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```

### `process_updated_events`
Stores updated list of events and and doesn't process past events
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
| system_id | | String | 
| events | | | Array(PlaceCalendar::Event)
#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```

### `send_event_email`
Sends event email reminder
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
| events | | | Array(PlaceCalendar::Event)
| system_id | | String
#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```
### `apply_filter`
Applies event filter
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
| events | | | Array(PlaceCalendar::Event)
#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```
### `select_todays_events`

#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
| events | | | Array(PlaceCalendar::Event)
#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```
### `update_network_user_password`
For cisco network credentials
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
| user_email | | String| 
| password | | String| 
| network_group_ids | | | [] of String

#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```
### `create_network_user`
For Cisco network credentials
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
| user_email | | String| 
| password | | String| 
| group_ids | | | [] of String


#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```