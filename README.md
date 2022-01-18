# What is Life Tracker?

Life Tracker is a simple markdown based tracker for your life. It provides a mechanism for recording your accomplishments, goals and retrospectives allowing you to keep track of your progress throughout the year and nail those performance reviews.

It aims to be as minimal as possible running off a flat-file system and a few scheduled actions. Leaving you with the freedom to do whatever you want with it, no more vendor lock-in or subscription fees, just simple file based recording.

## Recommended Usage

To get the most out of Life Tracker, we still recommend that you fork the repository on github to make use of the scheduled actions that are provided. This will allow you to receive email reminders for the recording of your goals, accomplishments and retrospectives.

Our secondary motivation for remaining on github is to allow you to leverage the inbuilt file editor for updating your life tracker. This removes the need for having a hard copy on your machine which you then require to perform updates.

## Installation

To install Life Tracker, simply fork the repository and perform the following steps:

1. Navigate to the **Settings > Secrets** page for the respository you just forked.
2. Add the following mandatory secrets:
   1. **MAIL_HOST:** The hostname of your mail server. (e.g. smtp.gmail.com)
   2. **MAIL_PORT:** The port of your mail server. (Typically 465)
   3. **MAIL_USERNAME:** Your accounts username on the mail server. (e.g. reminders@example.com)
   4. **MAIL_PASSWORD:** Your accounts password on the mail server.
   5. **TO_ADDRESS:** The email address to send the reminder to. (e.g. john@example.com)
   6. **FROM_ADDRESS:** The email address to send the reminder from. (e.g. "Reminders" \<reminders@example.com\>)
3. That's it!

## Notes for using a gmail account for sending mail

It's possible to use your own gmail account for sending reminders to yourself however it may not work if you have a gmail account that is not set up to allow less secure apps.

To enable less secure apps, go to [https://myaccount.google.com/lesssecureapps](https://myaccount.google.com/lesssecureapps) and enable it.

Following this you may also need to bypass captcha for sending mail, to do so navigate to [https://accounts.google.com/DisplayUnlockCaptcha](https://accounts.google.com/DisplayUnlockCaptcha) and follow the instructions.

In the event that your account is using 2FA you will also need to create an application specific password for your account. This can be done by following the instructions provided at the following article: [https://support.google.com/accounts/answer/185833?hl=en](https://support.google.com/accounts/answer/185833?hl=en)

Once the relevant changes have been made you should be able to use your gmail account for sending mail with the following secrets configured:

   1. **MAIL_HOST:** smtp.gmail.com
   2. **MAIL_PORT:** 465
   3. **MAIL_USERNAME:** \<username\>@gmail.com
   4. **MAIL_PASSWORD:** \<password\> or \<app-password\>

## Roadmap

- [ ] Stop disabled actions from causing a failed action run which subsequently sends an email.
- [ ] Allow configuration of different intervals for the different item tracking types.

## License

Life Tracker is distributed under the [MIT license](LICENSE.txt).

## Contact

If you would like to get in touch and discuss improvements or other ideas feel free to either raise an issue or contact me at the following email address:

Lucas Smith - me@lucasjamessmith.me
