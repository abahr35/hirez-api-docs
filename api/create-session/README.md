
## Create Session
>A required step to Authenticate the developer Id/signature for further API use.

Create a new authentication Session ID for requests that require authentication.

The [``Session``](./../README.md#session-authentication) is contained in an element called “<i>``session_id``</i>”. This parameter is needed to call the other methods.

With exception of [``CreateSession``](#create-session) and [``Ping``](./../ping#ping), all endpoints require authentication, so there is no concept of unauthenticated calls and rate limits.

<h2>URI Parameter</h2>

**Request**: <i>/**CreateSession**[response_type]/{dev_id}/{signature}/{timestamp}</i> `GET`
<table>
  <thead>
    <tr>
      <th style="width: 30%">Field</th>
      <th style="width: 10%">Type</th>
      <th style="width: 70%">Description</th>
      <th style="width: 30%">Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align='center'>response_type</td>
      <td align='center'>String</td>
      <td>A valid <a href="./../api-parameter-details.md#response-type" title="Response Type">Response Type</a></td>
      <td align='center'>“json”</td>
    </tr>
    <tr>
      <td align='center'>dev_id</td>
      <td align='center'>Integer</td>
      <td>The dev_id from your <a href="./../api-parameter-details.md#credentials" title="Credentials">Credentials</a></td>
      <td align='center'>1004</td>
    </tr>
    <tr>
      <td align='center'>signature</td>
      <td align='center'>String</td>
      <td>The generated <a href="./../api-parameter-details.md#signature" title="Signature">Signature</a> of <b>“CreateSession”</b> method</td>
      <td align='center'>“2bd92e62f3703da55f8b117f8a6228bd”</td>
    </tr>
    <tr>
      <td align='center'>timestamp</td>
      <td align='center'>String</td>
      <td>A valid <a href="./../api-parameter-details.md#timestamp" title="Timestamp">Timestamp</a></td>
      <td align='center'>“20191128030916”</td>
    </tr>
  </tbody>
</table>

<!--https://apidocjs.com/
  https://github.com/viniciuschiele/flask-apidoc/blob/master/flask_apidoc/apidoc.py
<table>
	<tr>
		<th>URI Parameter</th>
		<th>Description</th>
		<th>Example</th>
	</tr>
	<tr>
		<td>response_type</td>
		<td>A valid <a href="./../api-parameter-details.md#response-type" title="Response Type">Response Type</a></td>
		<td>“json”</td>
	</tr>
	<tr>
		<td>dev_id</td>
		<td>The dev_id from your <a href="./../api-parameter-details.md#credentials" title="Credentials">Credentials</a></td>
		<td>“1004”</td>
	</tr>
	<tr>
		<td>signature</td>
		<td>The generated <a href="./../api-parameter-details.md#signature" title="Signature">Signature</a> of <b>“CreateSession”</b> method</td>
		<td>“2bd92e62f3703da55f8b117f8a6228bd”</td>
	</tr>
	<tr>
		<td>timestamp</td>
		<td>A valid <a href="./../api-parameter-details.md#timestamp" title="Timestamp">Timestamp</a></td>
		<td>“20191128030916”</td>
	</tr>
</table>
-->

### Response

**JSON**
```json
{
 "ret_msg":"Approved",
 "session_id":"4D3064CF27D0473CA4CF142330E97FB5",
 "timestamp":"11/28/2019 3:09:16 PM"
}
```

**XML**
```XML
<Session xmlns="http://schemas.datacontract.org/2004/07/PaladinsApi" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
 <ret_msg>Approved</ret_msg>
 <session_id>4D3064CF27D0473CA4CF142330E97FB5</session_id>
 <timestamp>11/28/2019 3:09:16 PM</timestamp>
</Session>
```

#### Details
<table>
  <thead>
    <tr>
      <th style="width: 30%">Field</th>
      <th style="width: 10%">Type</th>
      <th style="width: 70%">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align='center' class="code">ret_msg</td>
      <td align='center'>String</td>
      <td><a href="./../README.md#ret-msg-approved" title="ret_msg">ret_msg</a></td>
    </tr>
    <tr>
      <td align='center'>session_id</td>
      <td align='center'>String</td>
      <td>The received <a href="./../README.md#session-authentication" title="Session">Session</a>. This parameter is needed to call the other methods.</td>
    </tr>
    <tr>
      <td align='center'>timestamp</td>
      <td align='center'>Date</td>
      <td><a href="./../api-parameter-details.md#timestamp" title="Timestamp">Timestamp</a></td>
    </tr>
  </tbody>
</table>
