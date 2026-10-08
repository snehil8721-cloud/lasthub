# StreamHub (Cloudinary storage) - Render deployment

1. Push this folder to GitHub, create a Render Web Service: Build `npm install`, Start `npm start`.
2. Render > Environment: set `CLOUDINARY_CLOUD_NAME`, `CLOUDINARY_API_KEY`, `CLOUDINARY_API_SECRET`. Optional: `UPLOAD_PASSWORD`, `DATA_DIR=/var/data` (needs a persistent disk, otherwise the video list resets on redeploy).
3. Open `/api/status` - `cloudinaryConfigured` should be `true`.
4. Upload from the site. Files go straight from the browser to Cloudinary.

Note: Cloudinary free plan limits a single video to 100 MB. Never commit secrets.
