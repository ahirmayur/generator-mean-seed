# Backend (Node) API Routes

Go to [server]/api/help - for example, `http://localhost:3000/api/help`.
There are subpages for each "group" of calls. These should be documented on the main help page, but in general each namespace has its own page. For example, the `Auth` module's calls may be found at `http://localhost:3000/api/auth/help`.

NOTE: for security/authorization, all backend calls should be checked (to ensure a user is logged in and has privileges to complete the request specified). To simulate this for the api/help, type your authority keys into the URL and they'll be read at GET params. For example, either using the interative help login call OR the site itself, login. A `user_id` and `sess_id` are return; set these in the URL as GET params (i.e. `?user_id=38asdlfk3&sess_id=alkjefe3dk`) and they'll be passed back on all calls to authenticate. Note - this still will NOT give you access to ALL calls UNLESS you're a super admin. Super admins fields on the user object must be manually set in the database (to prevent other people from making themselves a super admin).