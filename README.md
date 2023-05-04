Download Link: https://assignmentchef.com/product/solved-cs50-project3-single-page-app-email-client
<br>
Using JavaScript, HTML, and CSS, complete the implementation of your single-page-app email client. You must fulfill the following requirements:

<ul>

 <li><strong>Send Mail</strong>: When a user submits the email composition form, add JavaScript code to actually send the email.

  <ul>

   <li>You’ll likely want to make a POSTrequest to /emails, passing in values for recipients, subject, and body.</li>

   <li>Once the email has been sent, load the user’s sent mailbox.</li>

  </ul></li>

 <li><strong>Mailbox</strong>: When a user visits their Inbox, Sent mailbox, or Archive, load the appropriate mailbox.

  <ul>

   <li>You’ll likely want to make a GETrequest to /emails/&lt;mailbox&gt; to request the emails for a particular mailbox.</li>

   <li>When a mailbox is visited, the application should first query the API for the latest emails in that mailbox.</li>

   <li>When a mailbox is visited, the name of the mailbox should appear at the top of the page (this part is done for you).</li>

   <li>Each email should then be rendered in its own box (e.g. as a &lt;div&gt;with a border) that displays who the email is from, what the subject line is, and the timestamp of the email.</li>

   <li>If the email is unread, it should appear with a white background. If the email has been read, it should appear with a gray background.</li>

  </ul></li>

 <li><strong>View Email</strong>: When a user clicks on an email, the user should be taken to a view where they see the content of that email.

  <ul>

   <li>You’ll likely want to make a GETrequest to /emails/&lt;email_id&gt; to request the email.</li>

   <li>Your application should show the email’s sender, recipients, subject, timestamp, and body.</li>

   <li>You’ll likely want to add an additional divto html (in addition to emails-view and compose-view) for displaying the email. Be sure to update your code to hide and show the right views when navigation options are clicked.</li>

   <li>See the hint in the Hints section about how to add an event listener to an HTML element that you’ve added to the DOM.</li>

   <li>Once the email has been clicked on, you should mark the email as read. Recall that you can send a PUTrequest to /emails/&lt;email_id&gt; to update whether an email is read or not.</li>

  </ul></li>

 <li><strong>Archive and Unarchive</strong>: Allow users to archive and unarchive emails that they have received.

  <ul>

   <li>When viewing an Inbox email, the user should be presented with a button that lets them archive the email. When viewing an Archive email, the user should be presented with a button that lets them unarchive the email. This requirement does not apply to emails in the Sent mailbox.</li>

   <li>Recall that you can send a PUTrequest to /emails/&lt;email_id&gt; to mark an email as archived or unarchived.</li>

   <li>Once an email has been archived or unarchived, load the user’s inbox.</li>

  </ul></li>

 <li><strong>Reply</strong>: Allow users to reply to an email.

  <ul>

   <li>When viewing an email, the user should be presented with a “Reply” button that lets them reply to the email.</li>

   <li>When the user clicks the “Reply” button, they should be taken to the email composition form.</li>

   <li>Pre-fill the composition form with the recipientfield set to whoever sent the original email.</li>

   <li>Pre-fill the subject If the original email had a subject line of foo, the new subject line should be Re: foo. (If the subject line already begins with Re: , no need to add it again.)</li>

   <li>Pre-fill the bodyof the email with a line like “On Jan 1 2020, 12:00 AM <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="4c2a23230c29342d213c2029622f2321">[email protected]</a> wrote:” followed by the original text of the email.</li>

  </ul></li>

</ul>


