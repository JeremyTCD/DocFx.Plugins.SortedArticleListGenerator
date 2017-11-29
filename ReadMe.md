**This ReadMe is incomplete (work in progress)**  
# DocFx SortedArticleListGenerator
[![Build status](https://ci.appveyor.com/api/projects/status/3gt21k5ah72ae31p?svg=true)](https://ci.appveyor.com/project/JeremyTCD/docfx-plugins-sortedarticlelistgenerator)
<!--- Add test status once badge with logo is available https://github.com/badges/shields/pull/812 --->

A [DocFx](https://dotnet.github.io/docfx/) plugin.

#### Table of Contents  
[Summary](#summary)  
[Getting SortedArticleListGenerator](#getting-sortedarticlelistgenerator)  
[Usage](#usage)  
[Detailed Explanation](#detailed-explanation)  
[Building](#building)  

## Summary
A DocFx post-processor for article list generation. SortedArticleListGenerator sorts articles by date, extracts snippets from each article and inserts the resulting list of snippets into one or more articles.

## Getting SortedArticleListGenerator

## Usage
### Including Articles In The Sorted Article List
Articles to be included must have two Yaml values:
- jr.date: Value must be in the month/day/year format, e.g 12/8/2017.
- jr.includeInSal: Value must be true.

Optionally, an article can have a third optional value:
- jr.salSnippetLength: Value must be the number of characters to include. The default snippet length is 500. 
<!--todo article must have article element with id _content-->
Example article that SortedArticleListGenerator will include:
```YAML
---
jr.date: 12/8/2017
jr.includeInSal: true
---

# Your Article Header
...
```  
<!--todo example template-->

### Inserted The Sorted Article List
The sorted list of articles is inserted into any html page generated from an article that meets the following requirements:
- jr.insertSal with value true.
- Generated html page must have a div element with id sal-all-items. 

Example article that SortedArticleListGenerator will insert the sorted article list into:
```YAML
---
jr.insertSal: true
---

# Your Article Header
...
```  
A div with id sal-all-items must be added to the Liquid/Mustache template you are using for your articles.
<!--todo example template-->

## Detailed Explanation

## Building

## License
[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/JeremyTCD/JeremyTCD.github.io/dev/License.txt)  
