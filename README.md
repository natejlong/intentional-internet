
# intentional-internet

*Use the internet as the *tool* it ought to be.*

-----



## Table of Contents

1.  [What this is](#org420d6bd)
2.  [How it works](#org8a481b7)
3.  [Installation](#org0015fe5)
    1.  [Manual](#orgbafd038)
4.  [What this blocks](#orga78bbe7)
    1.  [Supported](#org447e976)
    2.  [Don&rsquo;t support](#org49a1035)
5.  [Contributing](#orge95968b)
6.  [Issues](#org30a97b4)
7.  [Why this exists](#orgb110d30)



<a id="org420d6bd"></a>

## What this is

Some sites are designed to get you to spend as much time on them as possible. Using them to complete a particular task is an exhausting process of fighting their attempts to distract you. This project blocks these distractions so you can accomplish your original intention as efficiently as possible.

See [What this blocks](#orga78bbe7) for more details.


<a id="org8a481b7"></a>

## How it works

It uses existing ad-blocking tools you probably have already installed. It just gives them more rules for what to block. Note, however, that while ad-blockers are careful not to touch actual website content, this project *will* block real content.

Technically speaking, it&rsquo;s a single text file with a list of EasyList-compatible rules that can be added to various ad-blocking tools such as uBlock.


<a id="org0015fe5"></a>

## Installation


<a id="orgbafd038"></a>

### Manual

Included below is a link to uBlock&rsquo;s instructions for manually adding a custom filter list, but the same process applies to other adblock systems.

Specific instructions for tools not listed here are welcomed! Please file a PR to add them.

-   [uBlock: Filter Lists > Adding Manually](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists#adding-manually)


<a id="orga78bbe7"></a>

## What this blocks

This is best explained by describing the **intentions** we do and don&rsquo;t support. If you want to browse the internet with intentions we don&rsquo;t support, you will not like this tool.

For a more granular view, read through the list itself. Rules will have comments next to them explaining what they block.


<a id="org447e976"></a>

### Supported

-   Searching for specific content. (e.g. searching Amazon for a product)
-   Browsing lists of content you completely control. (e.g. your Twitter feed)


<a id="org49a1035"></a>

### Don&rsquo;t support

-   Undirected browsing of content. (e.g. browsing YouTube&rsquo;s homepage)
-   Viewing content recommendations (e.g. YouTube&rsquo;s &ldquo;Related&rdquo; video sidebar)


<a id="orge95968b"></a>

## Contributing

Contributions are greatly welcomed and we prioritize speedy reviews. Any rule, on any site, that aids our Supported Intentions can be added.

Contributed rules should come with the following information:

1.  An explanation in the PR of what is blocked (with links to examples).
2.  A mention of whether it works on both desktop and mobile, or only one.
3.  A mention of any significant trade-offs that come with blocking this content. Sometimes the content is clearly worth blocking, other times it&rsquo;s more of a gray area and ought to be discussed first.

The rules themselves should:

1.  Be specific enough that they *only* block unsupported content.
2.  Be as future-proof as possible.
    1.  Not accepted:
        1.  Rules targeting randomly generated class/id names
        2.  Rules targeting a generic, complicated DOM path (e.g. `div > div > div > span > div`)
3.  Have a short comment alongside the rule describing what it is meant to block


<a id="org30a97b4"></a>

## Issues

First, remember that this list is *meant* to be aggressive. It *will* block real content. It is not necessarily a bug if sites look strange/broken.

If you feel something is not working as intended, though, absolutely file an issue and explain the problem. Reporting issues helps improve the project just as much as any other contribution!


<a id="orgb110d30"></a>

## Why this exists

Our use of the internet could be described as one of two categories:

1.  Unintentional access: browsing content at random looking for something interesting.
2.  Intentional access: having a specific question you are using the internet to answer, looking for a *specific* piece of content.

Modern website design is frighteningly good at category #1, but at the cost of category #2.

For example, let&rsquo;s say you want to watch a specific video on YouTube.

1.  You open up youtube.com, and the screen is filled with exciting thumbnails and catchy titles, all distracting you from the video you opened the site to watch in the first place.
2.  You ignore all of that, and search for and successfully find the video you want.
3.  You click on the video
4.  A page-long list of *other* videos pops up aiming to make you go watch those instead.
5.  A comments section by-default opens up with a huge amount of low quality content you weren&rsquo;t using the site to see.
6.  You finally just watch the video (though it may be interrupted by ads during it as well).
7.  The video ends. You now have 10 seconds to exert free will before the site will forcibly start a new video for you.
8.  Repeat every time you want to watch some content on YouTube.

A good tool is one that helps you accomplish *your* task with maximum efficiency. The above UX is not that of a good tool.

It doesn&rsquo;t respect the task you are trying to use it for, and it actively tries to make you spend *more* time on the task, not less.

Now, nothing about this is *evil* nor is there some conspiracy to suppress thought or anything so ridiculous. It&rsquo;s simply:

1.  Natural business incentives.
    
    The group of people called YouTube make money from advertising. Success comes mainly from people spending as much time using the site (and thus, viewing ads) as possible. Reality is not so black-and-white cynical, of course, and they certainly do care about genuinely helping people, but there are competing incentives at play.

2.  Too much of a good thing
    
    Imagine you build a product, release it, and it&rsquo;s a huge success; everyone loves it. What do you do next? Do you:
    
    1.  Build and release an even better v2 designed to increase everything that people loved about the first one.
    2.  Declare that the first version was good enough, *too* good even, and refuse to make anything resembling it ever again.
    
    You picked option A. We all did. If the first product obviously improved people&rsquo;s lives enough to inspire such adoption, making an even better version must improve the world that much more.
    
    However, if your v1 happened to be called &ldquo;OxyContin&rdquo;, &ldquo;Marlboro cigarettes&rdquo;, or &ldquo;slot machines&rdquo;, then unfortunately the improve-the-world option actually turned out to be the destroy-some-lives option.
    
    Now of course YouTube is not an opioid; I don&rsquo;t intend these as strong analogies. The point, though, is that the same principle applies to all product design, and here too. We humans have *good-enough* free will, not *perfect* free will, and every now and then a product comes along that is so &ldquo;good&rdquo; that we struggle to moderate our use of it and it actually becomes unhealthy.

So we end up with a bunch of websites that offer great utility, but are perhaps a bit *too* good at catching our attention to the detriment of our original intention for using them.

A word on intentions, too. At an individual level, distraction is a minor annoyance, but nothing so catastrophic as I might be making it out to sound, right? All on our own, we humans lose our trains of thought and get distracted all the time. These external distractions are hardly novel, so why does this project even exist?

Well, let me put it this way. Accidental distraction is simply part of life, yes. *Intentional* distraction doesn&rsquo;t have to be, though.

Humanity isn&rsquo;t &ldquo;done&rdquo;. We have much work to do. Poverty, disease, malnourishment, death, climate change, war, etc. are all problems that humans are working to solve everyday. If the group of people called Amazon distract some retiree into buying a new cat toy instead of the book they were meaning to order, no big deal. However, if a cancer researcher ends up wasting two hours on YouTube when they only meant to watch a 10-minute video before bed, that just directly slowed down human progress.

That&rsquo;s all it is. We have work to do and problems to solve; we all benefit by helping each other accomplish our intentions, and we all suffer by slowing each other down with needless distractions. Eventually this will be realized and even companies will understand the universal benefit that comes from helping the human machine run efficiently. Until then, this project is a drop of oil smoothing the same gears.

