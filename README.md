<p align=center>
<a href="https://empllo.com">
<img src="https://res.cloudinary.com/dnfmabyz2/image/upload/v1677752836/remotely_site_banner_s3yp5z.png"/>    
</a>
</p>

# Tech Jobs Feeds

## About empllo.com
We're one of the fastest growing Tech Job Board (https://empllo.com)

At Empllo, we use XML feeds:
* to share our own live tech jobs with our community
* to receive tech jobs to publish from our partners

So whether you are a developper interested in our data or a partner willing to share tech jobs with us, and you want to do so using XML feed(s), then you are in the right place!

## I/ Getting Empllo's live tech jobs: our feeds by category

Please note that XML Feed documentation and access is granted so that developers can share our jobs further. Please do not submit Empllo jobs to third Party websites, including but not limited to: Jooble, Neuvoo, Google Jobs, LinkedIn Jobs. 

**Please link back to the URL found on Empllo AND mention empllo.com as a source in order to Empllo to get traffic from your listing**. If you don't do that, we'll be forced to terminate your access, sorry! 

Our feed with most recent tech jobs across categories
- https://empllo.com/feeds/tech-jobs.rss

Here are XML feeds by job categories:
- [Sotware Development](https://empllo.com/feeds/remote-development-jobs.rss)
- [Product](https://empllo.com/feeds/remote-product-jobs.rss)
- [Business & Management](https://empllo.com/feeds/remote-business-management-jobs.rss)
- [Finance](https://empllo.com/feeds/remote-finance-jobs.rss)
- [Design](https://empllo.com/feeds/remote-design-jobs.rss)
- [Data](https://empllo.com/feeds/remote-data-jobs.rss)
- [Marketing](https://empllo.com/feeds/remote-marketing-jobs.rss)
- [Operations](https://empllo.com/feeds/remote-operations-jobs.rss)
- [Sales](https://empllo.com/feeds/remote-sales-jobs.rss)
- [Legal](https://empllo.com/feeds/remote-legal-jobs.rss)
- [HR & People](https://empllo.com/feeds/remote-hr-people-jobs.rss)
- [Customer Support](https://empllo.com/feeds/remote-customer-support-jobs.rss)
- [Writing](https://empllo.com/feeds/remote-writing-jobs.rss)
- [All Others](https://empllo.com/feeds/remote-other-jobs.rss)

## II/ Sharing tech jobs with Empllo

If you are a Empllo's partner and want to share tech jobs with us automatically through XML feed, you are in the right place!

We are working with our partners both with:
* organic/free tech jobs feeds 
* premium/paid-for tech jobs feed

Get in touch with us at hello@empllo.com for more details and to share your feed(s) with us.

### 1. Expected Data to be made available on feed

At Empllo we are interested to display jobs:
- That are 100% tech-related
- Mostly permanent positions (full-time, part-time, contract), less temporary freelance gigs
- In English language
- Mostly in IT domain / tech / web / software companies (see our job categories on https://empllo.com)

Empllo usually gets XML feed data with open job positions matching these criteria.

It is expected that positions listed at a given time are opened at that time. In other words, when Empllo fetches the XML feed URL, only open positions should be listed. 

Job listings that are not open anymore are expected to be removed from the list. Empllo will detect the jobs that were removed from the list and will remove it from its website (if it was published on Empllo’s website).

### 2. Data Format

Empllo expects the data in XML format. 
See our category feeds above for a live example.
Typical data structure should like like this (you may have different XML tag names, which is OK):

```xml
<?xml version='1.0'?>
<data>
   <jobs>
       ## 1 <job> entry for each job listing
       <job>
           ######### REQUIRED FIELDS ##########
           # A unique ID across your system that will allow Empllo to identify this job listing
           <job-id>002e1ea7bb19</job-id>

           # The job title
           <title>
               Backend Developer
           </title>

           # URL redirectiog to the job listing detail page on your website
           <url>
               https://url.that-redirects.to-your-job.listing.page
           </url>

           # Publication date should be provided for GMT timezone. E.g for 1st of September 2020 at 14:00:00 GMT:
           <publication-date>
               2020-09-01T14:00:00Z
           </publication-date>

           # The full HTML job description, wrapped into a "CDATA"
           <description>
               <![CDATA[
                   <h1>Job Description</h1>
                   <p>We are looking for ....</p>
               ]]>
           </description>

           # Name of company hiring
           <company-name>
               Empllo
           </company-name>

           # The job category. A mapping between your categories and Empllo's category may be discussed.
           <category>
               Software Development
           </category>

           ######### OPTIONAL FIELDS ##########
           # This is a string providing location restriction for the remote candidate
           <candidate-location-restriction>
               North America only
           </candidate-location-restriction>

            # This is a string providing location of the company offices, eg:
           <hq-location>
               New York, NYC, USA
           </hq-location>

           # One of the following values: full_time/part_time/contract/freelance/internship/other.
           # A mapping between your job types and Empllo's job types may be discussed.
           <job-type>
               full_time
           </job-type>

           # URL to the company logo
           <company-logo>
               https://url/to/the/company/logo.png
           </company-logo>

           # Short text describing the company hiring
           <company-description>
               Empllo helps IT professionals land remote jobs.
           </company-description>

           # Salary description. Recommended:The best format is $USD per year with no other text.
           <salary>
               $40-50K per year
           </salary>
       </job>
   </jobs>
</data>


```
