## Coding Task

Design and implement a URL shortener backend using Cloudflare Workers, PlanetScale, and Clerk.dev for user authentication. Your code will reside in `your_full_name/coding_tasks` folder.

### Features:

1. **URL Shortener (Custom and Random):** Implement endpoints to create short URLs. When creating a short URL, the user could specify a custom short identifier or have the system generate a random one.

2. **Analytics:** For each visit to a short URL, record analytics data such as the visitor's geographic location, device type, and browser. This data can be extracted from the HTTP request headers and the IP address.

3. **URL Redirector:** Create a special route that allows users to create a short URL from a list of provided URLs. When this short URL is accessed, it should randomly redirect the user to one of the URLs from the original list.
4. **User Authentication:** Use Clerk to implement user registration and authentication. Each user would have their own collection of short URLs. When creating or retrieving a short URL or its analytics data, ensure that the authenticated user is the owner of the short URL.

5. **URL Expiration:** When creating a short URL, the user could optionally specify an expiration time. Store this expiration time in the PlanetScale database along with the short URL. When a short URL is visited, check if the current time is past the expiration time and, if so, return an error instead of performing the redirect.