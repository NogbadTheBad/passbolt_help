---
title: How to update my subscription key
slug: update-evaluation-subscription-key
layout: faq
category: hosting
permalink: /faq/hosting/:slug
date: 2019-05-27 00:00:00 Z
---
## Step by step guide

Whether you want to replace your evaluation key with a subscription key, or update your subscription key with a new one you can follow the steps below.

### Get ready
All the commands provided below should be done from inside your passbolt directory.
```bash
$ cd /var/www/passbolt
```

### Steps
Passbolt Pro currently does not provide a UI to manage subscription keys.

To update your subscription key, you need to replace your previous subscription key with the new one.
In passbolt, the subscription key is stored in `/var/www/passbolt/config/license`

To replace the existing subscription key with the new one:

```bash
$ cp -u path_to_your_new_subscription_key config/license
```

To check if the operation was successful and if the new subscription key is valid:

```bash
$ bin/cake passbolt license_check
```

If your key is valid, this command will display the passbolt logo.