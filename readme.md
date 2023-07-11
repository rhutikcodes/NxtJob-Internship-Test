# Let's get Internship Ready!

👋🏽 Hello there! Congratulations on being shortlisted for an internship opportunity at NxtJob. This document outlines your task, which should be ideally submitted within 5 days.

## Next Steps

To advance in this opportunity, complete the following tasks and submit a PR (Pull Request) to this repository.

Firstly, clone this repository or download it as a zip file. Inside the repository, you'll find a folder named `intern_challenge`. Make a copy of this folder and rename it to your full name, using snake_case for spaces (for instance, john_doe). Inside this folder, you will find two `'answers.txt'` files located in the `'technical'` and `'non_technical'` subfolders. Edit these files with your responses.

The coding task should be executed within a subfolder named `'coding_tasks'`. Start by initializing your backend project here.


## Technical Questions

1. Attach a prisma.schema or schema.ts (Drizzle) file from one of your past projects where you have used Prisma or Drizzle ORM.
2. Explain, in your own words, the difference between "Edge Serverless" and "Serverless".
3. Describe when and where you usually encounter bugs in your development process.
4. Discuss the importance of maintaining clean and readable code. What best practices do you follow to structure and write code for ease of reading?


## Non-Technical Questions

1. How do you stay updated on backend development topics and remain active in the community? (Forums/Discord/Slack/Meetups/Twitter/Blogs)
2. What are your most-used IDE and keyboard shortcuts when coding?
3. How do you approach the design and implementation of a scalable backend system? Feel free to attach code snippets for better explanation.

## Coding Task

Design and implement a URL shortener backend using Cloudflare Workers, PlanetScale, and Clerk.dev for user authentication. Your code will reside in `your_full_name/coding_tasks` folder.

### Features:

1. **URL Shortener (Custom and Random):** Implement endpoints to create short URLs. When creating a short URL, the user could specify a custom short identifier or have the system generate a random one.

2. **Analytics:** For each visit to a short URL, record analytics data such as the visitor's geographic location, device type, and browser. This data can be extracted from the HTTP request headers and the IP address.

3. **URL Redirector:** Create a special route that allows users to create a short URL from a list of provided URLs. When this short URL is accessed, it should randomly redirect the user to one of the URLs from the original list.
4. **User Authentication:** Use Clerk to implement user registration and authentication. Each user would have their own collection of short URLs. When creating or retrieving a short URL or its analytics data, ensure that the authenticated user is the owner of the short URL.

5. **URL Expiration:** When creating a short URL, the user could optionally specify an expiration time. Store this expiration time in the PlanetScale database along with the short URL. When a short URL is visited, check if the current time is past the expiration time and, if so, return an error instead of performing the redirect.

