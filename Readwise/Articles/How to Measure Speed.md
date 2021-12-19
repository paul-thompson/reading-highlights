# How to Measure Speed

**Author:** web.dev  
**Full title:** How to Measure Speed?  
**URL:** https://web.dev/how-to-measure-speed/  
**Source:** #articles #instapaper #readwise

- Real-world performance is highly variable due to differences in users' devices, network connections, and other factors 
   
- Lab data is performance data collected within a controlled environment with predefined device and network settings 
   
- Field data is performance data collected from real page loads experienced by your users in the wild. Each type has its own strengths and limitations. 
   
- Lab data offers reproducible results and a debugging environment, but might not capture real-world bottlenecks and cannot correlate against real-world page KPIs 
   
- With lab data, you need to understand your users' typical devices and networks and appropriately mirror those conditions when you test performance. 
   
- Field data (also called Real User Monitoring or RUM) captures true real-world user experience and enables correlation to business KPIs, but has a restricted set of metrics and limited debugging capabilities 
   
- Lighthouse takes a URL and runs a series of audits against the page, generating a report on how well the page did. 
   
- Chrome User Experience Report (CrUX) provides metrics showing how real-world Chrome users experience popular destinations on the web. 
   
- PageSpeed Insights provides both lab and field data about a page. It uses Lighthouse to collect and analyze lab data about the page, while real-world field data is based on the Chrome User Experience Report dataset. 
   
