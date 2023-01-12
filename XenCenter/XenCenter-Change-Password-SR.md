Change password of Samba share (CIFS storage repository) in XenCenter CLI:
XenCenter Passwort von Storage repository(SR) ändern:
1) Get ID of cifspassword_secret of the SR via:xe pbd-list
2) xe secret-param-set uuid=SECRET_ID value=NEW_PASSWORD
3) xe pbd-unplug uuid=SR_UUID
4) xe pbd-plug uuid=SR_UUID

Username per edit of /var/xapi/state.db possible?