tidal.wav — Album Submission Demo

What this contains:
- A minimal Express app that serves a frontend form to submit album metadata + audio files
- Stores files under /uploads/<submission-id> and metadata in data/submissions.json
- Simple admin dashboard to review submissions, play audio in-browser, approve/reject, and download a ZIP containing audio files and metadata.

Quick start:
1. npm install
2. (optional) set ADMIN_PASS environment variable, e.g. export ADMIN_PASS="mysecret"
3. npm start
4. Visit http://localhost:3000 to submit an album
5. Visit http://localhost:3000/admin/login to sign in as admin (password from ADMIN_PASS or default "adminpass") and review submissions.

Notes:
- This is a demo. Files are stored on the local filesystem; for production use, move storage to a proper object store (S3/etc), add CSRF protection, rate limiting, stricter auth, virus scanning and proper audio processing.
- Cover image is checked client-side to meet the 3000x3000 minimum, but server-side validation is recommended in production.