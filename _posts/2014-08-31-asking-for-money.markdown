---
layout: post
title:  "Behind the Design: FullStory Onboarding"
date:   2014-08-31 22:45:17
---
One of the screens I'm most proud of in FullStory is the first one that customers see as onboarding kicks off: The credit card screen.

![Alt text](/assets/fs_onboarding_cc.png "Optional title")

>Hold on, Josh. Why in the world do you ask for a credit card as part of onboarding?
>
>—You, the reader

...I had the same reservations. Would we be asking too much? But given FullStory's infancy, we're not quite to the point where the floodgates can be opened to any and every website. Instead, we're carefully trying to learn all we can from each of the people that go through the trial. We weren't sure it would work, but asking for a credit card up front has reaped the right kind of benefits for us, including:

- **It helps keep out the tire-kickers.** We only have so much time and focus at our disposal — so we want a strong signal from customers with enough of a drive that they'd plunk down a credit card to try something.
- **It set's an expectation that FullStory is a *for-pay* product.** While we've discussed freemium plans and the like, we're not to the point where we could even entertain it in earnest — simply because of the scale at which we're having to do things on the backend.
- **It establishes accountability.** Perhaps the 14-day trial constraint does this more, but I also think that having a steeper onboarding process increases our internal feeling of accountability. They're trusting us with their credit card, after-all. 

## Breaking down the design
From a visual design point of view, there's not a whole lot going on. It's a simple three-color design in a two-column layout with one primary goal: Get the user through the credit card hurdle and into the product. The form has your focus, with the supporting copy right-aligned.

### The form
I'm particularly happy with the treatment of the form. It reduces down strictly to the required pieces of information — billing address, for example isn't requested. 

![Alt text](/assets/form_detail.png "Optional title")

The top input represents the email provided to us when a user signs up — it's read-only at this point, thus the italicized style. "Create a Password" was intentionally labeled as such because as we're providing the email address up top, I didn't want people to think they'd already been given a password. Short version: "Password" wasn't verby enough. 

Name, credit card number, expiration, and CVC, all rest on a light-gray box to subtly reinforce the transaction's security. I read a great blog post a year or two ago that outlined one developer's attempt at increasing sales simply by refining the billing form over and over again — a bounding box around the most sensitive information was called out as a benefitial step. You're establishing credibility and trust with this step.

### Form interaction design details
It's important that users can tab through the inputs with their keyboard, but the more you customize the inputs, the trickier it gets to represent the focus state. I'm happy with the solution we implemented here: Focus is represented by highlighting the right border (border-right: 1px solid $blue) of the password, name, and credit card number fields. The bottom select inputs (month & year), as well as the CVC field each show focus with a via their bottom borders. It's simple, stylized, and does the job.

![Alt text](/assets/form_focus.gif "Optional title")

### Supporting copy
I won't bore you with details about the copy on this particular page, except to say it went through more than 15+ revisions. The copy needn't be long because there's only a couple things to say, and also because reading a right-aligned block of text isn't that fun. 

>It turns out that having the layout of the page dictate right-aligned text was a fortuitous design constraint on the copy.

### Earlier concepts
I found a few concepts that preceeded the final design we shipped. Before we were confident enough to gate entrance on billing information we toyed with an ability to postpone filling out the billing form. "Snoozing" the credit card request would allow users to set up their site if they didn't have their card handy.

![Alt text](/assets/cc_form_snooze.png "Optional title")

This last one shows the form as a modal dialog upon choosing a plan. While visually interesting and direct, the 1px line connecting the billing form to the copy was overkill since there was no other copy competing for attention.

![Alt text](/assets/cc_form_modal.png "Optional title")

> While visually interesting and direct, the 1px line connecting the billing form to the copy was overkill since there was no other copy competing for attention.

## What we could do better
As with everything, there's always room to learn and improve. The thing is *never* done. And in this case, the crop is ripe for the picking. 