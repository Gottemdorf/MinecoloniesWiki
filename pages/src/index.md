---
title: MineEnemies
layout: default
--- # Um hello! I'm not a programmer or anything so i don't really understand a lot of whats going on with this file i'm editing here but i was hoping to request an addition to the mod/suggest an addition if possible! Its okay if not, I just thought it would be interesting. I feel like most people I know that enjoy this mod really love the building aspect of it, but once finished it feels like there isn't much left to do with the colony. The PVP system is a really cool idea and can be a lot of fun! however in my experience most gamers prefer to avoid the possibility of their hard-built colony getting destroyed, although they like doing the destroying themselves/combat experience... (funny how that works). This sparked an idea. I noticed that in the most recent version of minecolonies, mini abandoned colonies can be found like villages all over the world. I think it would be so fun and add a lot of adventure to the game if there was some way to create natrually spawned colonies in the world, and that through diplomacy the player might hve the option to ally themself with this colony or to perhaps gain enough favor to take over said colony as their own! Or the player might (with a gurgle of delight) conquer said colony subsequentially decide to add it to their kingdom or raze it to the ground. This would provide an endless drive to explore the world even in a single player setting/world and entertain beyond the foundation of a colony. However, if the player went to war with said colony but failed to conquer it quickly, then said colony might launch a raid on the player's own base with increased difficulty in comparrison to usual attacks from raiders. Another idea is that these auto-generated colonies i've coined as "mine enemies" (get it because they're my enemies) could grow proportionately to the size of the player's own existing colony. This might be a stretch, but I think it would make the game more lastingly fun. For example, if my town hall is level 1 still and I have a population of 10, the AI run colonies i encounter might also have a similar level and population, give or take a bit. If I have a maxed colony, and have conquered or allied myself with a few other colonies, expanding into a kingdom, then the colonies I make war with might bring allies of their own into the fray. Maybe this could cause waves of attacks during an enemy raid from a warring colony instead of one large wave, like in a pillager raid. Please consider adding mine enemies to your mod- that would really blow it out of the water for me and my friends! Thank you for all you do!
# Welcome to the MineColonies Wiki!

MineColonies is an interactive building mod that allows you to create your own thriving town within Minecraft. It lets your leadership skills soar by providing you with everything you need to build your kingdom. MineColonies gives you the flexibility to create a colony as unique as every player. With so many options, you’ll create a different colony every time, adapt it to any biome, build inside a mountain, on top of one, under the ocean, or in the sky.

The limit is your imagination!

MineColonies features NPC workers such as [Builders](../../source/workers/builder), [Farmers](../../source/workers/farmer), [Fishers](../../source/workers/fisher), [Foresters](../../source/workers/forester), [Miners](../../source/workers/miner), [Smelters](../../source/workers/smelter), [Bakers](../../source/workers/baker), [Cooks](../../source/workers/cook), [Couriers](../../source/workers/courier), five types of animal herders, [Composters](../../source/workers/composter), and many more, with even more being developed and added as the mod grows.

It also includes specialized buildings such as the [Warehouse](../../source/buildings/warehouse), [House](../../source/buildings/house), [Town Hall](../../source/buildings/townhall), [Barracks](../../source/buildings/barracks), [Library](../../source/buildings/library), [University](../../source/buildings/university), and even the [School](../../source/buildings/school).

### Please note that the wiki is a work in progress and will usually refer to the latest 1.18.2 and&#47;or 1.19.2 alpha version of MineColonies!

<hr />

<div class="row">
{% for item in site.data.subnav.subnav %}
    <div class="col-lg col-md-3 col-sm-12 text-center">
        <h3 class="button p-1">{{ item.title }}</h3>
        {% case item.type %}
            {% when "buildings" %}
                {% for entry in site.data.buildinginfo %}
                    {% building_link entry[0] %}<br />
                {% endfor %}
            {% when "workers" %}
                {% assign grouped = site.data.workerinfo | group_by_exp: "item", "item[1].type | default: 'default'" %}
                {% for group in grouped %}
                    {% unless forloop.first %}
                        <br/>
                    {% endunless %}
                    <span>{{ site.data.workertypes[group.name].name }}</span><br/>
                    {% for entry in group.items %}
                        {% worker_link entry[0] %}<br />
                    {% endfor %}
                {% endfor %}
            {% else %}
                {% for entry in item.subitems %}
                    <a href="{{ entry.url | relative_url }}">{{ entry.page }}</a><br />
                {% endfor %}
        {% endcase %}
    </div>
{% endfor %}
</div>

<hr />

MineColonies is a free and open-source mod developed by Let's Dev Together (LDT), a non-profit community. The source code is available on [GitHub](https://github.com/ldtteam/minecolonies). Our developers are a hard-working, well-integrated coding team, continuously adding more content to make the MineColonies experience even greater. However, we are always looking for more people to contribute to the mod, whether as a coder, builder, artist, voice actor, wiki editor, tester, or simply supporting us on [Patreon](https://www.patreon.com/minecolonies)!

Found a bug? Report it as an [issue](https://github.com/ldtteam/minecolonies/issues/new/choose) to help us give you the best gaming experience. If you require any help or just want to join the conversation, check us out on [Discord](https://discord.minecolonies.com)!
