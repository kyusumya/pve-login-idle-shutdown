#!/bin/bash

last_login_time=$(journalctl -u pvedaemon --since "1 days ago" | grep "successful auth for user")

if [ -z "$last_login_time" ]; then
    /sbin/shutdown -h now
fi
