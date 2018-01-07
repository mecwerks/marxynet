---
layout: default
permalink: contact
title: Contact
---
<div align="left">
<h3>
To submit bug reports, please visit <a href="https://github.com/mecwerks/marxynet/issues">marxynet</a> on GitHub. <br><br>

For steam account association, please fill out the following fields, and press "Submit" (Max 3).
</h3>

<ul>
  <li><strong>Page Link</strong>: enter the link you want your page to be referenced by, for example enter "none" to use SteamAccount #1 or enter a name. Your page will be accessable from "marxy.net/players/[Page Link]"</li>
  <li><strong>Display Name</strong>: The name to display at the top of your player page.</li>
</ul>

<form name="customplayer" netlify>
    <label>Page Link<font color="red">*</font>: <input type="text" name="uid"  placeholder="none" required></label><br>
    <label>Display Name<font color="red">*</font>: <input type="text" name="name"  placeholder="Mary the Hacker" required></label><br>
    <label>Steam Account ID #1<font color="red">*</font>: <input type="text" name="steamidOne" placeholder="76561198104649119" required></label><br>
    <label>Steam Account ID #2: <input type="text" name="steamidTwo" placeholder="76561198393693567"></label><br>
    <label>Steam Account ID #3: <input type="text" name="steamidThree"></label><br>
    <label>Note: <input type="text" name="note" placeholder="Thank 4 web"></label>
  <p>
    <button type="submit">Submit</button>
  </p>
</form>

<font color="red">*</font> = Required fields
</div>
