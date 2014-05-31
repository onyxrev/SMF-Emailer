# SMF Emailer

A stupid script that runs 'svcs' for you at some interval and checks to see whether your services are happy.  If they aren't it emails you.  I wrote this because, unfortunately, SmartOS' set-notify functionality is incomplete.

Yeah, it's ruby so it's about 35MB of RAM when it's running.  Derp.

## Installation

I put smf_emailer in /opt/local/bin and smf_emailer.yml in /opt/local/etc

### ruby
Install ruby your preferred way.  If you don't have a preferred way this works:

```
pkgin install ruby200
```

### gems
You can either run the "gem" command:

```
gem install eventmachine mail
```

or if you prefer pkgin:

```
pkgin install ruby200-eventmachine ruby200-mail
```

### SMF
Included is a sample xml file for running SMF Emailer via SMF

### Config
Also included is a sample YAML file.  The mail settings stanza is passed to the mail gem.  So any valid mail gem configurations should work.
