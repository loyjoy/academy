## Appointment

Offer customers in the chat to make appointments in well-defined time slots.

![appointment_demo](https://raw.githubusercontent.com/loyjoy/welcome/master/help/processes/process/subprocesses/appointment_demo.png)

**Email notification** - You can have an email sent automatically to your own email (not your customers email) as a notification.

**Email content** - You can use any variables in the PDF and HTML template by using the correct notation (${...}). If you don't have a template, you can just type the text. If you use plain text, it will not be formatted in any way.

**Time slots** - Slots are defined bot-wide, i.e. are shared between experiences of a bot so that potential appointments do not collide. To use the same calendar in different experiences, the calendar name must be the same.

You have to add time slots for the process module to work properly.

![appointment_calender_demo](https://raw.githubusercontent.com/loyjoy/welcome/master/help/processes/process/subprocesses/appointment_calender_demo.png)

Make sure to use the correct timezone. The default is set to UTC±0.

![appointment_scheduler_timezone_demo](https://raw.githubusercontent.com/loyjoy/welcome/master/help/processes/process/subprocesses/appointment_scheduler_timezone.png)


**Time buffer** - You can add a time buffer to allow customers to book an appointment only up to X minutes before the actual appointment.
