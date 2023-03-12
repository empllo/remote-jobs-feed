<p align=center>
<a href="https://tryremotely.com">
<img src="https://res.cloudinary.com/dnfmabyz2/image/upload/v1677752836/remotely_site_banner_s3yp5z.png"/>    
</a>
</p>

# Remote Jobs Feeds

## About tryremotely.com
We're one of the fastest growing Remote Work Job Board (https://tryremotely.com)

At Remotely, we use XML feeds:
* to share our own live remote jobs with our community
* to receive remote jobs to publish from our partners

So whether you are a developper interested in our data or a partner willing to share remote jobs with us, and you want to do so using XML feed(s), then you are in the right place!

## I/ Getting Remotely's live remote jobs: our feeds by category

Please note that XML Feed documentation and access is granted so that developers can share our jobs further. Please do not submit Remotely jobs to third Party websites, including but not limited to: Jooble, Neuvoo, Google Jobs, LinkedIn Jobs. 

**Please link back to the URL found on Remotely AND mention tryremotely.com as a source in order to Remotely to get traffic from your listing**. If you don't do that, we'll be forced to terminate your access, sorry! 

Our feed with most recent remote jobs across categories
- https://tryremotely.com/feeds/remote-jobs.rss

Here are XML feeds by job categories:
- [Sotware Development](https://tryremotely.com/feeds/remote-development-jobs.rss)
- [Product](https://tryremotely.com/feeds/remote-product-jobs.rss)
- [Business & Management](https://tryremotely.com/feeds/remote-business-management-jobs.rss)
- [Finance](https://tryremotely.com/feeds/remote-finance-jobs.rss)
- [Design](https://tryremotely.com/feeds/remote-design-jobs.rss)
- [Data](https://tryremotely.com/feeds/remote-data-jobs.rss)
- [Marketing](https://tryremotely.com/feeds/remote-marketing-jobs.rss)
- [Data](https://tryremotely.com/remote-jobs/data/feed)
- [Operations](https://tryremotely.com/feeds/remote-operations-jobs.rss)
- [Sales](https://tryremotely.com/feeds/remote-sales-jobs.rss)
- [Legal](https://tryremotely.com/feeds/remote-legal-jobs.rss)
- [HR & People](https://tryremotely.com/feeds/remote-hr-people-jobs.rss)
- [Customer Support](https://tryremotely.com/feeds/remote-customer-support-jobs.rss)
- [Writing](https://tryremotely.com/feeds/remote-writing-jobs.rss)
- [All Others](https://tryremotely.com/feeds/remote-other-jobs.rss)

## II/ Sharing remote jobs with Remotely

If you are a Remotely's partner and want to share remote jobs with us automatically through XML feed, you are in the right place!

We are working with our partners both with:
* organic/free remote jobs feeds 
* premium/paid-for remote jobs feed

Get in touch with us at hello@tryremotely.com for more details and to share your feed(s) with us.

### 1. Expected Data to be made available on feed

At Remotely we are interested to display jobs:
- That are 100% remote
- Mostly permanent positions (full-time, part-time, contract), less temporary freelance gigs
- In English language
- Mostly in IT domain / tech / web / software companies (see our job categories on https://tryremotely.com)

Remotely usually gets XML feed data with open job positions matching these criteria.

It is expected that positions listed at a given time are opened at that time. In other words, when Remotely fetches the XML feed URL, only open positions should be listed. 

Job listings that are not open anymore are expected to be removed from the list. Remotely will detect the jobs that were removed from the list and will remove it from its website (if it was published on Remotely’s website).

### 2. Data Format

Remotely expects the data in XML format. 
See our category feeds above for a live example.
Typical data structure should like like this (you may have different XML tag names, which is OK):

```xml
<?xml version='1.0'?>
<data>
   <jobs>
       ## 1 <job> entry for each job listing
       <job>
           ######### REQUIRED FIELDS ##########
           # A unique ID across your system that will allow Remotely to identify this job listing
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
               Remotely
           </company-name>

           # The job category. A mapping between your categories and Remotely's category may be discussed.
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
           # A mapping between your job types and Remotely's job types may be discussed.
           <job-type>
               full_time
           </job-type>

           # URL to the company logo
           <company-logo>
               https://url/to/the/company/logo.png
           </company-logo>

           # Short text describing the company hiring
           <company-description>
               Remotely helps IT professionals land remote jobs.
           </company-description>

           # Salary description. Recommended:The best format is $USD per year with no other text.
           <salary>
               $40-50K per year
           </salary>

       </job>

   </jobs>
</data>


```
