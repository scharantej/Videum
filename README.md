## Flask Application Design: Video Player with Grid and Details Page

### HTML Files
1. **Main Page (index.html)**
   - Contains a grid of videos with thumbnails, titles, and brief descriptions.
   - Each video has a link to the details page.
   - Includes a header and footer for consistent design across all pages.

2. **Details Page (details.html)**
   - Displays a single video's details, including its title, description, and a video player.
   - Offers options to play, pause, mute, and adjust the volume of the video.
   - Allows users to navigate back to the main page.

### Routes
1. **Home Route ('/')**
   - Renders the main page (index.html).

2. **Details Route ('/details/<video_id>')**
   - Accepts a video ID as a parameter.
   - Fetches the video data from the database using the provided ID.
   - Renders the details page (details.html) with the retrieved video data.

3. **Video Playback Route ('/play_video/<video_id>')**
   - Accepts a video ID as a parameter.
   - Streams the video file associated with the provided ID.

4. **Video Information Route ('/video_info/<video_id>')**
   - Accepts a video ID as a parameter.
   - Returns the video's title, description, and duration in JSON format.
   - This route can be used by external applications to retrieve video information.