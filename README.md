# Forge API Reference (FAR)

Exploring data storage in forge repositories, ideally in browser-based apps.

## GitHub

<table>
<tbody>
<tr>
<td>
	<b>personal access token fine-grained</b>
</td>
<td rowspan="2">
	<ul>
		<li>per-user setup</li>
		<li>developer-oriented</li>
	</ul>
</td>
<td>
	<ul>
		<li>('permissions'-based)</li>
		<li>git over https</li>
	</ul>
</td>
</tr>
<tr>
<td>
	<b>personal access token classic</b>
</td>
<td>
	<ul>
		<li>(oauth scope-based)</li>
	</ul>
</td>
</tr>
<tr>
<td>
	<b>github/oauth app user token, web flow login</b>
</td>
<td rowspan="2">
	<ul>
		<li>per-app/dev setup</li>
		<li>simple end-user ux</li>
		<li>commits as user</li>
		<li>(github app tokens expire)</li>
		<li>(oauth app tokens valid until revoked)</li>
	</ul>
</td>
<td>
	<ul>
		<li>(intended for web apps)</li>
		<li>consumer secret implies developer server</li>
	</ul>
</td>
</tr>
<tr>
<td>
	<b>github/oauth app user token, device flow login</b>
</td>
<td>
	<ul>
		<li>(intended for headless)</li>
		<li>("cannot be used for browsers", no CORS)</li>
		<li>no consumer secret, only client id</li>
		<li>must present verification code in-app and ask user to enter on github.com</li>
	</ul>
</td>
</tr>
<tr>
<td>
	<b>github app installation token</b>
</td>
<td colspan="2">
	<ul>
		<li>per-app/dev setup</li>
		<li>simple end-user ux</li>
		<li>commits as app</li>
		<li>generating jwt with private keys feels complicated, maybe manageable; can use Octokit.js but it adds bloat</li>
	</ul>
</td>
</tr>
</tbody>
</table>

### Codeberg / Forejo / Gitea

<table>
<tbody>
<tr>
<td>
	<b>access token</b>
</td>
<td>
	<ul>
		<li>per-user setup</li>
    <li>developer-oriented</li>
	</ul>
</td>
</tr>
</tbody>
</table>
