# Main Concepts
## Application Levels
### App Instance
The _App Instance_ denotes the entire application at a hosting system level. It groups all the conceptual elements of the app entity, like _Teams_, _Pools_, _Users_, _Channels_, etc... The _App Instance_ is associated to a global _Admin_ (see _Users Level_ section bellow).

### Team
A _Team_ denotes a group of authenticable users and is administrated by one of them, the _Team Chief_ (see _User Levels_ section bellow). Every team have a unique name on the _App Instance_ and is associated to a _Pool_. Each user of the team grow that _Pool_ by uploading tracks,

### Channel
A _Channel_ denotes a virtual room administrated by the _Chief_ that authenticated users can join for listening to music and chat about it. Every channel is associated to a _Stream_, provided by the application back office (Liquidsoap)

## Role Levels
### Admin
The _Admin_ of the app have every possible rights. He can monitor each logic elements of the app (storage, networking, app configuration, etc...). He regulates physical resources of the hosting machine by restricting for example Disc Usage and CPU for each _Team_. The _Admin_ has the possibility to create a new _Team_ and promote a user as Chief.

### Chief
The _Chief_ denotes the "_Team_ admin". He has all rights in it, except for the restrictions set by the _Admin_ (f.e. number of _Channels_, of _Users_, storage limit, bandwidth, etc...). The _Chief_ can invite and accept request for creating new _Users_ and manage them, create new _Channel_, manage the _Pool_, edit meta-datas, remove tracks, and manage _Stream_ behaviours.

### User
The _User_ denotes the regular application user. The _User_ can be related to only one _Team_ (_User_ accounts aren't cross-_Team_). When unauthenticated, the _User_ can't do anything except log in or ask for the creation of a new account in a _Team_ to his related _Chief_. Once logged, the _User_ can join every _Channel_ of the _Team_, post messages in it and, the most important, get access to the _Stream_ attached to each _Channel_. Finally, he can also upload new audio files on the server adding them to the _Pool_.
