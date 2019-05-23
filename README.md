# ![LOGO](logo.png) Cloud Billing **flow**ground Connector

## Description

A generated **flow**ground connector for the Cloud Billing API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/cloudbilling/v1/swagger.json<br/>
Generated at: 2019-05-23T12:13:04+03:00

## API Description

Allows developers to manage billing for their Google Cloud Platform projects
    programmatically.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists the billing accounts that the current authenticated user has<br/>
> permission to [view](https://cloud.google.com/billing/docs/how-to/billing-access).

*Tags:* `billingAccounts`

#### Input Parameters
* `filter` - _optional_ - Options for how to filter the returned billing accounts.
Currently this only supports filtering for
[subaccounts](https://cloud.google.com/billing/docs/concepts) under a
single provided reseller billing account.
(e.g. "master_billing_account=billingAccounts/012345-678901-ABCDEF").
Boolean algebra and other fields are not currently supported.
* `pageSize` - _optional_ - Requested page size. The maximum page size is 100; this is also the
default.
* `pageToken` - _optional_ - A token identifying a page of results to return. This should be a
`next_page_token` value returned from a previous `ListBillingAccounts`
call. If unspecified, the first page of results is returned.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a billing account.<br/>
> This method can only be used to create<br/>
> [billing subaccounts](https://cloud.google.com/billing/docs/concepts)<br/>
> by GCP resellers.<br/>
> When creating a subaccount, the current authenticated user must have the<br/>
> `billing.accounts.update` IAM permission on the master account, which is<br/>
> typically given to billing account<br/>
> [administrators](https://cloud.google.com/billing/docs/how-to/billing-access).<br/>
> This method will return an error if the master account has not been<br/>
> provisioned as a reseller account.

*Tags:* `billingAccounts`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists all public cloud services.

*Tags:* `services`

#### Input Parameters
* `pageSize` - _optional_ - Requested page size. Defaults to 5000.
* `pageToken` - _optional_ - A token identifying a page of results to return. This should be a
`next_page_token` value returned from a previous `ListServices`
call. If unspecified, the first page of results is returned.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets information about a billing account. The current authenticated user<br/>
> must be a [viewer of the billing<br/>
> account](https://cloud.google.com/billing/docs/how-to/billing-access).

*Tags:* `billingAccounts`

#### Input Parameters
* `name` - _required_ - The resource name of the billing account to retrieve. For example,
`billingAccounts/012345-567890-ABCDEF`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates a billing account's fields.<br/>
> Currently the only field that can be edited is `display_name`.<br/>
> The current authenticated user must have the `billing.accounts.update`<br/>
> IAM permission, which is typically given to the<br/>
> [administrator](https://cloud.google.com/billing/docs/how-to/billing-access)<br/>
> of the billing account.

*Tags:* `billingAccounts`

#### Input Parameters
* `name` - _required_ - The name of the billing account resource to be updated.
* `updateMask` - _optional_ - The update mask applied to the resource.
Only "display_name" is currently supported.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the billing information for a project. The current authenticated user<br/>
> must have [permission to view the<br/>
> project](https://cloud.google.com/docs/permissions-overview#h.bgs0oxofvnoo<br/>
> ).

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The resource name of the project for which billing information is
retrieved. For example, `projects/tokyo-rain-123`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Sets or updates the billing account associated with a project. You specify<br/>
> the new billing account by setting the `billing_account_name` in the<br/>
> `ProjectBillingInfo` resource to the resource name of a billing account.<br/>
> Associating a project with an open billing account enables billing on the<br/>
> project and allows charges for resource usage. If the project already had a<br/>
> billing account, this method changes the billing account used for resource<br/>
> usage charges.<br/>
> <br/>
> *Note:* Incurred charges that have not yet been reported in the transaction<br/>
> history of the GCP Console might be billed to the new billing<br/>
> account, even if the charge occurred before the new billing account was<br/>
> assigned to the project.<br/>
> <br/>
> The current authenticated user must have ownership privileges for both the<br/>
> [project](https://cloud.google.com/docs/permissions-overview#h.bgs0oxofvnoo<br/>
> ) and the [billing<br/>
> account](https://cloud.google.com/billing/docs/how-to/billing-access).<br/>
> <br/>
> You can disable billing on the project by setting the<br/>
> `billing_account_name` field to empty. This action disassociates the<br/>
> current billing account from the project. Any billable activity of your<br/>
> in-use services will stop, and your application could stop functioning as<br/>
> expected. Any unbilled charges to date will be billed to the previously<br/>
> associated account. The current authenticated user must be either an owner<br/>
> of the project or an owner of the billing account for the project.<br/>
> <br/>
> Note that associating a project with a *closed* billing account will have<br/>
> much the same effect as disabling billing on the project: any paid<br/>
> resources used by the project will be shut down. Thus, unless you wish to<br/>
> disable billing, you should always call this method with the name of an<br/>
> *open* billing account.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The resource name of the project associated with the billing information
that you want to update. For example, `projects/tokyo-rain-123`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the projects associated with a billing account. The current<br/>
> authenticated user must have the `billing.resourceAssociations.list` IAM<br/>
> permission, which is often given to billing account<br/>
> [viewers](https://cloud.google.com/billing/docs/how-to/billing-access).

*Tags:* `billingAccounts`

#### Input Parameters
* `name` - _required_ - The resource name of the billing account associated with the projects that
you want to list. For example, `billingAccounts/012345-567890-ABCDEF`.
* `pageSize` - _optional_ - Requested page size. The maximum page size is 100; this is also the
default.
* `pageToken` - _optional_ - A token identifying a page of results to be returned. This should be a
`next_page_token` value returned from a previous `ListProjectBillingInfo`
call. If unspecified, the first page of results is returned.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists all publicly available SKUs for a given cloud service.

*Tags:* `services`

#### Input Parameters
* `currencyCode` - _optional_ - The ISO 4217 currency code for the pricing info in the response proto.
Will use the conversion rate as of start_time.
Optional. If not specified USD will be used.
* `endTime` - _optional_ - Optional exclusive end time of the time range for which the pricing
versions will be returned. Timestamps in the future are not allowed.
The time range has to be within a single calendar month in
America/Los_Angeles timezone. Time range as a whole is optional. If not
specified, the latest pricing will be returned (up to 12 hours old at
most).
* `pageSize` - _optional_ - Requested page size. Defaults to 5000.
* `pageToken` - _optional_ - A token identifying a page of results to return. This should be a
`next_page_token` value returned from a previous `ListSkus`
call. If unspecified, the first page of results is returned.
* `parent` - _required_ - The name of the service.
Example: "services/DA34-426B-A397"
* `startTime` - _optional_ - Optional inclusive start time of the time range for which the pricing
versions will be returned. Timestamps in the future are not allowed.
The time range has to be within a single calendar month in
America/Los_Angeles timezone. Time range as a whole is optional. If not
specified, the latest pricing will be returned (up to 12 hours old at
most).
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the access control policy for a billing account.<br/>
> The caller must have the `billing.accounts.getIamPolicy` permission on the<br/>
> account, which is often given to billing account<br/>
> [viewers](https://cloud.google.com/billing/docs/how-to/billing-access).

*Tags:* `billingAccounts`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy is being requested.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Sets the access control policy for a billing account. Replaces any existing<br/>
> policy.<br/>
> The caller must have the `billing.accounts.setIamPolicy` permission on the<br/>
> account, which is often given to billing account<br/>
> [administrators](https://cloud.google.com/billing/docs/how-to/billing-access).

*Tags:* `billingAccounts`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy is being specified.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Tests the access control policy for a billing account. This method takes<br/>
> the resource and a set of permissions as input and returns the subset of<br/>
> the input permissions that the caller is allowed for that resource.

*Tags:* `billingAccounts`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy detail is being requested.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-cloudbilling-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
