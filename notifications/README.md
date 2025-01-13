# Notification Templates

The notification templates are stored in `notifications/` directory. The notification templates are a simple XML file which is registered automatically and are used for sending system notices via E-Mail, SMS, etc.

Notification files are XML in the format:

```
<NotificationTemplate xmlns="http://santedb.org/notification" lang="en" id="org.santedb.sample.notification.name">
    <subject>The Subject</subject>
    <![CDATA[This is a sample notification, properties can be placed in ${parameter}.]]>
</NotificationTemplate>
```