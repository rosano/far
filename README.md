# Forge API Reference (FAR)

Exploring data storage in forge repositories, ideally in browser-based apps.


[far.rosano.ca](https://far.rosano.ca).

## GitHub

<table>
<tbody>
<tr>
<td>
	<a href="https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#fine-grained-personal-access-tokens">personal access token fine-grained</a>
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
	<a href="https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#fine-grained-personal-access-tokens">personal access token classic</a>
</td>
<td>
	<ul>
		<li>(oauth scope-based)</li>
	</ul>
</td>
</tr>
<tr>
<td>
	<a href="https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/generating-a-user-access-token-for-a-github-app#using-the-web-application-flow-to-generate-a-user-access-token">github/oauth app user token, web flow login</a>
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
	<a href="https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/generating-a-user-access-token-for-a-github-app#using-the-device-flow-to-generate-a-user-access-token">github/oauth app user token, device flow login</a>
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
	<a href="https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/authenticating-as-a-github-app-installation">github app installation token</a>
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
	<a href="https://docs.codeberg.org/advanced/access-token/">access token</a>
</td>
<td>
	<ul>
		<li>per-user setup</li>
		<li>developer-oriented</li>
	</ul>
</td>
</tr>
<tr>
<td>
	<a href="https://forgejo.org/docs/latest/user/oauth2-provider/">oauth app user token</a>
</td>
<td>
	<ul>
		<li>per-app/dev setup</li>
		<li>simple end-user ux</li>
		<li>only works per instance (not federated)</li>
	</ul>
</td>
</tr>
</tbody>
</table>
