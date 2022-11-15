# SRE best practices
- don’t expect a tool to solve
- cultural change and need “believers” in senior role to advocate within company
- people need to absorb info within their own mindset

## “Reliability is a journey”
- it is a process that can span 6-9 months in orgs w/ 5000 engineers; nothing happens immediately
- Step 1: “I want to be reliable when I grow up” (you must believe you have problem first)
- Step 2: [“Read the book!”](https://sre.google/sre-book/table-of-contents/) and watch [SRE v DevOps](https://www.youtube.com/watch?v=0UyrVqBoCAU)
- Step 3: “Panic!” (myth: fire team and retrain; not the case and can retrain team in house)
- Step 4: Start small, be patient, celebrate each step - spread the word

## Common Language: traditionally, incentives aren’t aligned
- developers incentivized with rapid change (ship more)
- operators incentivized w/ stability (limit change)

## Latency:
- research in cognitive psychology ( human perception cannot tell diff w/ 3 9s to 4 9s )
- “art of an SLO” - figure out how much error budget we can still keep customers happy with
- not about number of 9s (not badge of honor) “we need to be good enough and keep our customers happy”
- it may be more beneficial to invest engineering efforts in features vs. more reliability
- defining goals is fundamental collaboration between dev and ops together

## CUJ (critical user journey)
- not everything needs to be measured (i.e. 3 clicks deep in left nav panel)

## Best practice:
- **Shared ownership** - reduce org silos
- **Error budgets** - accept failure as normal (blame is not helpful)
- **Reduce cost of failure** - implement gradual changes
- **Automate common case** - leverage tooling and automation (if you have a decision tree, or processes not written down, automation helpful)
- **Measure toil and reliability** - measure everything* (alert only on CUJ, but measure all)

## SLI (metrics)
- need to be very transparent in what we measure
- latency difficult end-to-end (browser through to load balancer and backend)

## SLO (SLI + goal) [internal]
- initial discussion “how many 9s can we achieve” (wrong approach)
- correct: what does success look like to customer and their expectation
- customer research, review report cases, measure actual experienced latency
- if lacking info: 1st goal should be current experience (current latency, availability)
- should be re-evaluated week 1, 4, 6 - first 6 weeks critical to nail down goals
- after 6 weeks, associate an alert to it (need it around long enough before too much noise)
- at least once/quarter re-evaluate; sit with all parties involved and decide whether to increase target
- SLOs have a life of their own; think about how to maintain over time (not set it and forget it)
- need to be meaningful to usage of customer; if customer use changes then need to change/evaluate
- avoid “collecting 9s as badge of honor”; starting with 3 9s is great (or even 2)

## SLA (adding consequences) [making some SLO public]
- our internal SLO exposed to public
- legal consequences; refund is strongest use case
- if you have an SLA, you should create stricter SLO and catch violations earlier (create error budget buffer)
- should not publish SLA to customer with unreasonable number of 9s
- should not publish SLA on something you historically fail on
- be very careful how you think about it to not erode trust of customers
- consider: global and local SLAs (CUJ for each: i.e. NA, EMEA, APAC)

## Myth: adoption of SLOs results in moving slower
- dev teams like receiving allowance for ice cream (spend all in 1 day, or spread it out)
- don’t spend budget, it’s taken away - if you don’t spend miss innovation opportunity (don’t horde it)
- gives opportunity to take risk without angering others
- historically if you don’t know budget, you become risk averse

## Benefit of error budgets
- Common incentives for DEVs and SREs - find right balance between innovation and reliability
- DEV teams can manage the risk themselves - they decide how to spend their error budget
- Unrealistic reliability goals are unattractive - dampen velocity of innovation
- DEV team becomes self-policing - error budget is valuable resource for them
- Shared responsibility for system uptime - infra failures eat into dev’s error budget

# Slides

## Overview
![Screen Shot 2021-05-13 at 9 13 56 AM](https://user-images.githubusercontent.com/5553105/118153292-f7fd2a80-b3d2-11eb-91ac-068bbdb7017c.png)

## Ingredients for success
![Screen Shot 2021-05-13 at 9 15 29 AM](https://user-images.githubusercontent.com/5553105/118153354-09decd80-b3d3-11eb-83d1-e3513bfbb4a3.png)

## Problem (incentive misalignment)
![Screen Shot 2021-05-13 at 9 16 23 AM](https://user-images.githubusercontent.com/5553105/118153431-21b65180-b3d3-11eb-9a9d-b3d41dd83b1e.png)

## Solution (shared language)
![Screen Shot 2021-05-13 at 9 20 56 AM](https://user-images.githubusercontent.com/5553105/118153489-309d0400-b3d3-11eb-8506-70d0a2f2c29c.png)

## Building blocks for reliable systems
![Screen Shot 2021-05-13 at 9 26 06 AM](https://user-images.githubusercontent.com/5553105/118153565-490d1e80-b3d3-11eb-915e-fdb95f9d9460.png)

## SRE best practices (personification of DevOps)
![Screen Shot 2021-05-13 at 9 27 08 AM](https://user-images.githubusercontent.com/5553105/118155344-60e5a200-b3d5-11eb-9c24-c8f68eb4902c.png)

## Terms
![Screen Shot 2021-05-13 at 9 39 54 AM](https://user-images.githubusercontent.com/5553105/118153686-6641ed00-b3d3-11eb-8bb6-c40594f47910.png)

## Benefits of error budgets (think ice cream allowance)
![Screen Shot 2021-05-13 at 9 51 20 AM](https://user-images.githubusercontent.com/5553105/118153715-6e9a2800-b3d3-11eb-9516-dac7ab6d3ce5.png)
