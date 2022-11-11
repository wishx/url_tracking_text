## How To Stop Links From Other Sites From Tracking You On Fediverse/Mastodon
A brief primer for beginners by @Derek I. Batting (@wishx@mastodon.social - https://mastodon.social/@wishx)

If you've been on any social networking sites, or let's be honest, the Internet in general, for more than 10 minutes, you've clicked a link to go to another website. It's how we navigate. What you might not know is that the sites you are on when you click that link might be adding tracking information to the link to follow you around the web and report back on what you see, how long you look at it, where you go from there and much, much more.

Today, I'm going to show you how they track you with this method, what to look for and how you can prevent it by "cleansing" URLs (links) of this tracking information.

First, an example of what I'm talking about. Let's say you see an article you're interested in, so you click it. Let's say it's this article:

`https://www.sciencemag.org/news/2018/10/chemists-find-recipe-may-have-jump-started-life-earth?utm_source=newsfromscience&utm_medium=facebook-text&utm_campaign=makingRNA-22081&fbclid=IwAR3NZaphbCAAaIdUpFGfg-X0uTevnObd7ole6mPI67yxmgcGPQt0AZOFY9Q`<br/>
*(Links intentionally made unclickable for this tutorial)*

After clicking on this link, you will get to your expected destination (in this case, an article on sciencemag.org), but what you might not know is that both Google and Facebook have now tracked you there and collected specific information, whether you have an account with them or not.

### How To Identify Click Tracking
Click Tracking comes after the actual end of a URL and usually begins with a question mark `?`. In the example above, the URL ends with the word "earth", then there is a ?utm=, then three Urchin/Google Analytics paramaters and one Facebook (fbclid=) tracker.

Multiple trackers can be added to a single URL by using `&` between them. For example, in the URL above, near the end you can see this: `&utm_campaign=makingRNA-22081&fbclid=IwAR3...` This is where Google tracking ends and Facebook tracking begins. So basically, you're being tracked all over the place whether you originally came from either of those sites or not. It doesn't even matter if you have Google or Facebook accounts. They're still collecting information.

### How To Cleanse A Link on Desktop and Mobile Browsers
Now that you know what to look for, you're going to want to strip this tracking information out before visiting the link so you aren't tracked. You'll also probably want to strip this information out before sharing links with others, whether here on Mastodon/Fediverse or elsewhere. There are a couple ways to accomplish this.

- **Manually (aka The Tedious Method):**<br/>
Right-click on the link and copy it to your Clipboard. Then paste it into the Address Bar of your browser, but don't hit Enter or visit the link yet.
Now, press the End key on your keyboard to go to the very end of the URL.
From there, start Backspacing until you've deleted all the way up to and including the `?`, then visit the site.

- **Automatically (aka Easy Peasy Method):**<br/>
Note: Only one of these should be necessary, but one may have features that another doesn't

Install the Neat URL extension for your browser.<br/>
Chrome, Chromium, Opera, Vivaldi, Brave: https://chrome.google.com/webstore/detail/neat-url/jchobbjgibcahbheicfocecmhocglkco<br/>
Firedox: https://addons.mozilla.org/en-US/firefox/addon/neat-url/<br/>
Open Source: https://github.com/Smile4ever/Neat-URL<br/>
An informative article about Neat URL: https://www.ghacks.net/2020/10/05/neat-url-is-an-extension-for-chrome-and-firefox-that-removes-tracking-elements-from-links/

Install CleanURLs extennsion for your browser.<br/>
Chrome, Chromium, Opera, Vivaldi, Brave: https://chrome.google.com/webstore/detail/clearurls/lckanjgmijmafbedllaakclkaicjfmnk<br/>
Firefox: https://addons.mozilla.org/en-US/firefox/addon/clearurls/<br/>
Open Source: https://gitlab.com/KevinRoebert/ClearUrls<br/>

Install the Tracking Token Stripper extension for your browser.<br/>
Chrome, Chromium or Opera: https://chrome.google.com/webstore/detail/kcpnkledgcbobhkgimpbmejgockkplob<br/>
Firefox: https://addons.mozilla.org/addon/utm-tracking-token-stripper/<br/>
Open Source: https://github.com/jparise/chrome-utm-stripper<br/>

There are browsers out there that claim to do this automatically such as Brave (`https://brave.com/index/`).<br/>
Brave is available for Windows 64-bit, Windows 32-bit, macOS and Linux. Also, Brave for Mobile is available on the Google Play Store, Apple App Store, Amazon and possibly F-Droid. 

## FAQ:
**Q:** Will cleansing links completely stop sites from tracking me?<br/>
**A:** It will prevent sites from tracking you *with URL click tracking only*. There are myriad other tracking methods out there such as cookies, tracking pixels, device fingerprinting, beacons, and more. For more information:<br/>
"Online Tracking - Federal Trade Commission, Consumer Information" - `https://www.consumer.ftc.gov/articles/0042-online-tracking`<br/>
"How do websites track users? | Technologies and methods | GDPR Compliance" - `https://www.cookiebot.com/en/website-tracking/`<br/>
"Web Tracking: What You Should Know About Your Privacy Online" - `https://medium.freecodecamp.org/what-you-should-know-about-web-tracking-and-how-it-affects-your-online-privacy-42935355525`

**Q:** Can websites still track me if I use a Private Tab or Incognito Mode on my browser?<br/>
**A:** Short answer: Yes. The only difference is that the cookie a site gives you once you land there will be deleted afterwards or the information they collect will be "generic" and see you as a "ghost user" with less or no other information about that particular visit. Keep in mind that this pertains to the site you are clicking *onto*, not where you came from. Remember, with Click Tracking, the tracking information is in the URL itself, so cookies really don't matter much here. That's why we want to strip that information out first.

**Q:** How can I prevent Android/iOS apps on mobile from tracking me this way?<br/>
**A:** If you are using a web browser on your mobile phone, you can copy the URL and paste it into the mobile browser, manually strip the tracking info, then go to the site. If you are using Chrome or Firefox for Mobile, certain tracking Extensions may also work on mobile. Maybe. If you are using a site's homegrown app (Instagram, Pinterest, Facebook, Facebook Messenger, etc.), you might be able to copy links out into a browser and strip out tracking info, but mobile is a whole other ballgame as far as tracking goes (GPS, cell tower triangulation, Advertiser IDs tied to your Google/Apple account, always-on microphones, etc.).

**Q:** Why should I bother cleansing URLs when posting them?<br/>
**A:** Because you're a good person and you care about your audience. That's probably why you shared the thing you posted in the first place. Think of it like this: Links are the sidewalk you use to walk from place to place around the Internet. If someone pastes a link on Mastodon/Fediverse with tracking information on it, it's like someone letting their dog poop on the sidewalk and leaving it for others to spread around on their shoes as they come and go. So, wipe the dog poop (the tracking ID) off your shoes before walking around (sharing or clicking on the link).

**Q:** Why doesn't Mastodon/Fediverse automatically strip out Third-Party Tracking from URLs for me when I post a link?<br/>
**A:** The short answer is that they don't tamper with your content in any way, for better or worse.  While each individual instance/server might implement features like this of their own accord, it isn't broadly done in the base software (to my knowledge and as of the time of this post).

**Q:** Are you some kind of tracking/privacy expert or something?<br/>
**A:** Not remotely. I'm just some dude on the Internet (albeit an IT professional with 30+ years experience) trying to educate you and others about tracking and how you can help keep it to a minimum here on Mastodon/Fediverse and potentially elsewhere.

**Sharing / Questions / Discussion / Pro Tips**
- Sharing: Please do! Spread it all over Mastodon/Fediverse if you like. That's why it's here. All I ask is that you share the first post in the thread with the full .TXT file and don't just copy/paste the message text.
- Questions / Discussion: Post them below.
- Pro Tips: If you know of other ways to help prevent tracking via URLs, let us know! I know there are a ton of useful anti-tracking, ad-blocking, HTTPS-forceing extensions and add-ons, and I use many of them myself, but this post is primarily about cleaning up URLs before posting them to Mastodon/Fediverse.

**Some Common Trackers**<br/>
(Not an exhaustive list)

- `?fbclid` - Facebook Click Identifier
- `?gclid` - Google Click Identifier - Exchange information between Google Analytics and Google AdSense
- `?mkt_tok` - Marketo click tracking
- `?utm_` - Urchin Tracking Module introduced by Google Analytics
- utm_source: Identifies which site sent the traffic, and is a required parameter.<br/>
Example: utm_source=Google
- utm_medium: Identifies what type of link was used, such as cost per click or email.<br/>
Example: utm_medium=cpc
- utm_campaign: Identifies a specific product promotion or strategic campaign.<br/>
Example: utm_campaign=spring_sale
- utm_term: Identifies search terms.<br/>
Example: utm_term=running+shoes
 -utm_content: Identifies what specifically was clicked to bring the user to the site, such as a banner ad or a text link. It is often used for A/B testing and content-targeted ads.<br/>
Example: utm_content=logolink or utm_content=textlink

Other common known trackers: `utm_source, utm_medium, utm_term, utm_content, utm_campaign, utm_reader, utm_place, utm_userid, utm_cid, utm_name, utm_pubreferrer, utm_swu, utm_viz_id, ga_source, ga_medium, ga_term, ga_content, ga_campaign, ga_place, yclid, _openstat, fb_action_ids, fb_action_types, fb_ref, fb_source, action_object_map, action_type_map, action_ref_map, gs_l, pd_rd_r@amazon., pd_rd_w@amazon., pd_rd_wg@amazon., _encoding@amazon., psc@amazon., ved@google., ei@google., sei@google., gws_rd@google., cvid@bing.com, form@bing.com, sk@bing.com, sp@bing.com, sc@bing.com, qs@bing.com, pq@bing.com, feature@youtube.com, gclid@youtube.com, kw@youtube.com, $/ref@amazon., _hsenc, mkt_tok, hmb_campaign, hmb_medium, hmb_source`

