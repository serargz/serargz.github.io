---
layout: post
title: "Fixing 'The following options failed to validate: SMBDirect' error in Metasploit"
description: ""
category:
tags: []
---
{% include JB/setup %}

This error is generated because the SMBDirect global variable is misconfigured. For some reason, when using the `smb_version` scanner in Metasploit (Kali), I received the error message:

    The following options failed to validate: SMBDirect

Its default value is `true`, so to configure it you should do:

    msf> setg SMBDirect true

This setting should fix the error.
