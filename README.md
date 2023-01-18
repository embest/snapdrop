# Snapdrop 

Snapdrop: local file sharing in your browser. Inspired by Apple's Airdrop.

With Caddy2

```
drop.xxxxx.xxx {
    root * /xxxxxxxxx/snapdrop/client

    file_server

    @snapdrop {
        header Connection Upgrade
    }

    reverse_proxy @snapdrop 127.0.0.1:3000

}
```