# GTM Cookie Manager Template

A Google Tag Manager template for managing cookies with advanced configuration options.

## Overview

This template provides a flexible way to manage cookies in Google Tag Manager with support for various cookie attributes and settings. It allows you to set, update, and manage cookies with fine-grained control over their behavior.

## Features

- Set multiple cookies with different configurations
- Control cookie expiration (days, months, years, or session)
- Configure SameSite attribute (lax, strict, none)
- Set HttpOnly flag
- Domain control
- Value encoding options
- Conditional cookie setting (if not set)
- Override existing values

## Configuration Options

### Cookie Settings

For each cookie, you can configure the following parameters:

| Parameter | Type | Description | Default |
|-----------|------|-------------|---------|
| Name | Text | Cookie name (required) | - |
| Value | Text | Cookie value | - |
| If not set | Checkbox | Only set if cookie doesn't exist | false |
| Encode Value | Checkbox | URL encode the cookie value | true |
| Override | Checkbox | Override value even if empty | false |
| Expiration | Text | Cookie lifetime | session |
| Domain | Text | Cookie domain | auto |
| SameSite | Select | SameSite attribute | - |
| HttpOnly | Checkbox | HttpOnly flag | false |

### Expiration Format

The expiration parameter accepts the following formats:
- `Xd` - X days (e.g., "30d" for 30 days)
- `Xm` - X months (e.g., "6m" for 6 months)
- `Xy` - X years (e.g., "1y" for 1 year)
- `session` - Session cookie (expires when browser closes)
- `0` - Delete the cookie

## Usage

1. Add the template to your GTM container
2. Configure the cookies you want to manage using the parameter table
3. Set the desired options for each cookie
4. Deploy the tag in your GTM container

## Security Features

- Secure flag is always enabled
- Configurable SameSite attribute
- Optional HttpOnly flag
- Value encoding option

## Notes

- The template automatically sets the path to "/"
- Domain defaults to "auto" which uses the current domain
- Empty values are only set if the "Override" option is checked
- Cookies are only set if they don't exist when "If not set" is enabled
