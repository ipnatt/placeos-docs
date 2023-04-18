---
title: PlaceOS Bookings Notifier
description: Access this System's Bookings data, via the Mailer Driver
---

# PlaceOS Bookings Notifier Driver
* Type: Logic Driver
* Dependencies: PlaceOS Driver
* Source: https://github.com/PlaceOS/drivers/blob/master/drivers/place/booking_notifier.cr

## Functions

* Notifies a user when a booking is taking place
* Sends email notifications on bookings

## Settings

| Key | Type | Default value | Description |
| --- | --- | --- | --- |
|`timezone`| String | "Australia/Sydney" 
|`date_time_format`| String | "%c"
|`time_format`| String | "%l:%M%p"
|`date_format`| String | "%A, %-d %B"
|`debug`| Boolean | false
|`booking_type` | String | "desk"
|`disable_attachments`| Boolean | true
|`poll_bookings`| Boolean | false
|`poll_every_minutes`| Int32 | 5
|`notify`
zone_id1
|`name`| String | "Sydney Building 1" 
|`email`| String | ["concierge@place.com"]
|`notify_manager`| Boolean | true
|`notify_booking_owner` | Boolean | true
|`include_network_credentials`| Boolean | false
`network_password_length` | | DEFAULT_PASSWORD_LENGTH
`network_password_exclude` | | DEFAULT_PASSWORD_EXCLUDE
`network_password_minimum_lowercase` | | DEFAULT_PASSWORD_MINIMUM_LOWERCASE
`network_password_minimum_uppercase` | | DEFAULT_PASSWORD_MINIMUM_UPPERCASE
`network_password_minimum_numbers` | | DEFAULT_PASSWORD_MINIMUM_NUMBERS
`network_password_minimum_symbols` | |DEFAULT_PASSWORD_MINIMUM_SYMBOLS
`network_group_ids` | | [] of String
zone_id2
`name` | String | "Melb Building"
`attachments` | | {"file-name.pdf" => "https://s3/your_file.pdf"}
`notify_booking_owner`| Boolean | true
|`bookings_checked` | UInt64 | 0_u64
|`error_count`| UInt64 | 0_u64
|`disable_attachments` | Boolean | true
|`poll_bookings` | Boolean | false
|`poll_every_minutes`| Int32 | 5
|`notify_lookup`| | Hash(String, SiteDetails)


## Status Variables

### `bookings_checked`

### `last_error`

### `error_count`

## Commands

### `on_update`

#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
| booking_type | | String | "desk" |   |
| time_zone | | String | "Australia/Sydney"
| date_time_format | | String | "%c"
|time_format| String | |  "%l:%M%p"
|date_format| | String | "%A, %-d %B"
| debug | | Boolean | false
|notify_lookup | | | 
|disable_attachments | | Boolean| true
|poll_bookings| | Boolean | 
|poll_every_minutes| | Int32 | 


#### Response Schema
```
```

#### Example Responses
##### 1. If successful:
```
```
### `parse_booking`

### `get_building_name`
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
|zones| | Array(String) | 

### `get_attachment`
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
|file_name| | String | 
| uri | | String

### `check_bookings`
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
|months_from_now| | Int32 | 2  

### `perform_booking_check`
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
|building_zone| |  
|building_name| |
|building_key| |
|emails| |
|notify_manager| |
|attachments| |
|months_from_now| | Int32 | 2


### `get_manager`
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
|staff_email| | String 

### `update_network_user_password`
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
|user_email | | String | 
|password| | String | 
|network_group_ids | | Array(String)

### `create_network_user`
#### Parameters
| Name | Required? | Type | Default | Description |
| --- | --- | --- | --- | --- |
|user_email | | String | 
|password| | String | 
|group_ids | | Array(String)

