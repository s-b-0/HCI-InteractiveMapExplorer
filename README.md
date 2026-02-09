# HCI-InteractiveMapExplorer

**HCI Analysis: Interactive Map Exploration Site by Sarah Benkoussa**

## Goals and Motivation

A project to highlight human-computer interaction (HCI) best-practices through an interactive website. This site showcases designs that ensure technology is user-friendly, intuitive, and effective to a target audience. Users will explore the New York City boba cafe scene using interactive maps and graphs.

Users will explore the New York City boba cafe scene. It will give the audience a light-hearted experience and a deeper look at where they can find boba and how they might want to drink it. This naturally diverges into two main goals: to discover bubble tea locations across NYC, and to learn about their optimized drink.

## Intended Use Case

The intended audience is NYC locals or visitors who are interested in learning more about bubble tea in the area and how to drink it. Users will be able to see an overall view of boba shops in NYC, then narrow down to a specific shop based on their preferences.

Then, after exploring where they can find bubble tea, viewers will learn about how to drink the tea based on personal habits.

## Related Materials

<https://observablehq.com/@kristw/boba-science>

The above article heavily inspires the site's second visualization. However, my chart is distinct in its mathematical formulas/calculations, as well as the weights/values of the sliders and how those sliders affect a given area on the chart.

The implementation is distinct as well. The methods and code used to build the graph, the areas, updating functions for the areas, etc. are all original.

## Data Source

**NYC JSON:** <https://github.com/nycehs/NYC_geography/blob/master/NTA.topo.json>

**Boba shops dataset:** <https://github.com/mebauer/boba-nyc/blob/master/teaapp/store_neighborhoods.csv>

The JSON data was used directly. As for the stores csv file, I used a python notebook for data transformation into a more easily digestible format.

## Design Iterations

The initial design was as follows: the page will open with a title and a brief paragraph to introduce users to the page’s subject. After scrolling through the text, viewers will reach the first visualization: the interactive map. This consists of two main components: a zoomable map & and a side panel for filters. The map will focus on NYC only. Tea shops will populate on both the larger main map and the mini map in the corner. Users can pan, drag, and zoom in on the map (which will be reflected in the mini map by a box highlighting the current view area). This mini-map view-box will also be draggable, so users can navigate to various portions of the map while maintaining the same zoom-level and a holistic view of where they are currently viewing relative to all of NYC.

Dots on the map can be hovered over to see more details such as rating, name, and price range. The dot will bolden/enlarge/change in some way to indicate interaction. Each dots will have a clickable feature that takes users to the shop’s website.

The side panel allows users to filter by borough or category (checkboxes).

After interacting with the map, users can scroll down to read more information and transition to the next visualization: a boba drinking optimization graph. This area chart allows users to input their drink’s metrics (such as ingredient proportions or drinking habits) to see their projected optimized bubble tea consumption over time. The graph shows volume of ingredients (tea, boba, ice in different colors) per sip until drink completion. Users can experiment with different slider metrics to see how each measurement might affect their optimal drinking strategy.

Sliders were used instead of text-input to constrain values of each metric. Changes to the metrics are reflected immediately on the graph for a responsive design strategy.

### Further Design Analysis

The fonts, colors, and text are casual and inviting. The warm, neutral color scheme and conversational tone are meant to feel welcoming and comfortable for viewers.

The map filter interaction is form-like, where users can take time selecting what they like before submitting or clearing preferences. This provides further diversity in the kinds of interactions users can take: pan/zoom/etc. with the map body, clickable buttons with the filters, and eventually draggable sliders with the graph.

For the graph, color-coded sliders provide tightly-coupled changes to their respective chart areas. The interaction is immediately upon release (unlike the map, where the filters are submitted like a form). This was necessary to allow for instant changes to the volumes that users could notice distinctively. However, numerical values are not greatly emphasized in the visualization. For the sliders, it would likely be difficult to quantify vague preferences about drinking habits, thus the ends are marked with exclamations that users can slide to agree or disagree with. The values on the axes are also not particularly large, since meaning is mostly conveyed through the areas and their proportions to one another as they are altered.

## Final Design (with random shop hovered on map to see tooltip)

![Image](/static/BobaSite_screenie1.png)

![Image](/static/BobaSite_screenie2.png)

![Image](/static/BobaSite_screenie3.png)

![Image](/static/BobaSite_screenie4.png)
