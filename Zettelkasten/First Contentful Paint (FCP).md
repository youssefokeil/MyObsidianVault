Created on: 15-04-2025 15:06
Status: #idea
Tags: #BaRead #backend 
# First Contentful Paint (FCP)
>First Contentful Paint (FCP) is a performance metric that measures the time it takes for the first piece of content of the [[Document Object Model (DOM)]] to appear on a webpage.

### Why is it Important?
- Good indicator of the first improvement
- If a page stays blank for a couple of seconds, then the user will not know if anything is happening
### How to measure:
1. Use Chrome's DevTools \> Performance \> Timings, and you'll see information about your FCP and LCP
2. [PageSpeed Insights](https://pagespeed.web.dev/?utm_source=psi&utm_medium=redirect)
3. [GTmetrix | Website Performance Testing and Monitoring](https://gtmetrix.com/)
#### Rubrics:
- Can be the first loading screen
- the first change in website
- Company logo appears
### Criticism 
 1. It may take seconds of blank white screen for the User to see any meaningful content, however, if the user sees anything of a background change like a change in color it may offer  a better user experience.
	- That's why we use the [[First Paint (FP)]] metric
	- Change between FP and FCP should be unnoticeable
![[fp&fcp.png]]
2. [[Largest Contentful Page (LCP]], measure loading the largest element (often an image) to appear for the user
	- This gives the users what they came for
-----------------
# References
[What Is First Contentful Paint (FCP) & How to Improve It In 2024](https://nitropack.io/blog/post/first-contentful-paint-fcp#:~:text=TL%3BDR%3A%20First%20Contentful%20Paint,browser%20caching%2C%20and%20compress%20images.)