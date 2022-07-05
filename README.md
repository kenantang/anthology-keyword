# Automated Keyword Search in ACL Anthology

This tool enables automated search for relevant papers with keywords in the [ACL Anthology](https://aclanthology.org). 

One key challenge is that the returned number is unstable. After multiple searches, the minimal number is the stable one. The multiple searches are realized by switching between the two search options ("Relevance" or "Year of Publication"). The clicks are automated by [chromedriver](https://chromedriver.chromium.org), so please check that the local chromedriver has the same version as the browser before running the script (version 103 for this initial commit).

Still, the results are not guaranteed to be correct, even when the number of searches is set to 10. For example, at 07/04/22 the number of "subreddit" papers should be 31. For multiple runs with 10 as the number, only 108 is returned.

In order to (1) provide enough time for searching and (2) space the clicks so that the script is not immediately identified as a bot, the average time for each query is now around 20 seconds. When the script reports an error, you can manually open the webpage to see if a captcha is required. After submitting the captcha once by yourself, you should be able to run the script again.

Currently only the notebook version is available. Command line support would be added later.
