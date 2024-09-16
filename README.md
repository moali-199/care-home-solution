### TASK 1: Form to log complaints for a user and capture <email_address>, <details_text>, <IP address> and <time> of the person creating the complaint.

I created a Model-Driven App in which you can see an active list of complaints.

![image](https://github.com/user-attachments/assets/788d1f61-5d79-43d8-a51f-b4017c4e6e70)

A form was created also, to include the above details as required.

![image](https://github.com/user-attachments/assets/86feec39-83ec-4a72-aa5a-2227d9ad7459)

Upon saving the complaint; the complaint is given a number, etc. who it is created by, the email address of the user has to be typed in themselves, and the time is logged.

![image](https://github.com/user-attachments/assets/81abaaf9-b640-4f8c-b6ce-55aa1367c6f5)

### TASK 2: Look up the relative geographic position of the IP address, using the free API provided by https://ipgeolocation.io, capture latitude and longitude and record this against the complaint.

The cloud flow on Power Automate takes a minute to complete, whereby once refreshed - you can see the IP address, latitude and longitude captured against the complaint.

![image](https://github.com/user-attachments/assets/6e56396e-4ea7-429a-8bae-ff34309b7b5d)

This was done using Power Automate Automated Cloud Flow and use of the given API from IP Geolocation, shown in the below screenshot:

![image](https://github.com/user-attachments/assets/1b53dc12-e88b-46ba-9372-5d4eb911069d)

Having initialised the variables for IP Address, Longitude and Latitude - we are able to record that for each of the users.

### TASK 3: Send email notifications using the free API provided by https://sendgrid.com/solutions/email-api/smtp-service/ to the Inspector with the complaint information and a form for them to action the complaint

Created the flow to send email notifications using Outlook flow; instead of the API provided, as it was causing me issues when creating an account - therefore used Outlook instead!
This flow was simply, whenever a new complaint is added; to send an email to the specific inspector which in this case I've put down as my own email, as we don't have an inspector in this hypothetical.

![image](https://github.com/user-attachments/assets/f5e3a2e4-1aea-4458-9b9e-8ce65387cc32)

I've also included in there the complaint information, by using the <details_text> as described above, for the inspector to receive an email highlighting the issue like this.

![image](https://github.com/user-attachments/assets/8fc99c8b-3a64-4fa4-821d-2961f25e0f92)

Of course, there are other things that could have also been added - such as the user name etc. however, as per the task this was sufficient.
The inspector is told to refer to the same active complaints form, in order to action the complaint - although I could have created another form here, I believed the original form was sufficient too.

### TASK 4: Notify <email_address> that the inspector actioned the complaint when inspector completed it.

Once actioned is changed to "Yes" as shown on the screenshot below:

![image](https://github.com/user-attachments/assets/b726c343-d677-4596-8b33-2d11b1b3eb67)

Then the email notification is sent out to the user email address, which is shown like below:

![image](https://github.com/user-attachments/assets/f9f456ab-b532-413e-b4ad-0fcd57587270)

This is due to the third cloud flow - in which the notification to the user is shown.

![image](https://github.com/user-attachments/assets/72527a18-55d5-4d03-a0e2-daea8f6cd79f)

Which leads to the email being sent.
