IntercomNewMessages
===================

Publishes a signal for each new conversation created in Intercom. When the block starts up, it creates a local web server and endpoint to receive the messages from nio. It also creates a webhook in Intercom that is configured to send to your callback url. When the block stops, it delete the webhook from Intercom.

Properties
----------
- **callback_url**(string): Your publicly accessible url that Intercom can POST notifications to.
- **access_token**(string): Your Intercom Access Token. You will need to request an [extended scope](https://developers.intercom.com/docs/personal-access-tokens#section-extended-scopes) token from Intercom.
- **web_server**(object): Host, Port and Endpoint to launch your webserver where Intercom will POST notifications to.

Dependencies
------------
requests

Output
------

```
{'app_id': 'mz6gs2p0',
 'created_at': 1499900215,
 'data': {'item': {'assignee': {'id': None, 'type': 'nobody_admin'},
                   'conversation_message': {'attachments': [],
                                            'author': {'id': '554028790f941a3cb3000ddf',
                                                       'type': 'user'},
                                            'body': "<p>Chris, it's me "
                                                    'again. One more '
                                                    'test.</p>',
                                            'id': '114942241',
                                            'subject': '',
                                            'type': 'conversation_message'},
                   'conversation_parts': {'conversation_parts': [],
                                          'total_count': 0,
                                          'type': 'conversation_part.list'},
                   'created_at': 1499900215,
                   'id': '10768842031',
                   'links': {'conversation_web': 'https://app.intercom.io/a/apps/mz6gs2p0/inbox/all/conversations/10768842031'},
                   'metadata': {},
                   'open': True,
                   'read': True,
                   'tags': {'tags': [], 'type': 'tag.list'},
                   'type': 'conversation',
                   'updated_at': 1499900215,
                   'user': {'email': 'cbrackert@n.io',
                            'id': '554028790f941a3cb3000ddf',
                            'name': 'Chris Brackert',
                            'type': 'user',
                            'user_id': '109570106748577333422'}},
          'type': 'notification_event_data'},
 'delivered_at': 0,
 'delivery_attempts': 1,
 'delivery_status': 'pending',
 'first_sent_at': 1499900215,
 'id': 'notif_66fdce40-6755-11e7-bd38-bdda4aa19f1b',
 'links': {},
 'self': None,
 'topic': 'conversation.user.created',
 'type': 'notification_event'}
```
