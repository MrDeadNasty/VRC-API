VOSTOK RELAY CHAT API INTEGRATION KIT
For Vostok Relay Chat v1.9.1 or newer.

This VMZ is documentation/examples for mod authors.
It is NOT a runtime dependency.
It has no autoloads, no hooks, and no running scripts.

You can:

drop it into mods as a harmless reference pack, or
rename .vmz to .zip and copy the examples out.
Current API:

register_event_category(source, category, default_template, description, default_enabled)
post_registered_event(source, category, vars, world_event)
post_event(category, text, source, world_event)
list_registered_events()
unregister_event_category(source, category)

Template tokens supported:

{player}
{username}
{task}
{trader}
{event}

Older percent-style tokens are also supported in Vostok Relay Chat v1.9.1+:

%player%
%username%
%task%
%trader%
%event%

Recommended style:

{player} completed {task} for {trader}

world_event:

false = player event
true = world/system event with no player attribution

Examples included:

Area05JobBoard_Example.gd
VEmission_Example.gd
BTRHeliTotalWar_Example.gd
API_Needed.txt
Important:

Other mods still need to detect their own event and call the API.
Relay Chat does not automatically know when another mod event happens.

Thanks to improvise for the API
