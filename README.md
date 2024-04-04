jasiahpowers.com
*simple custom modern layout for a portfolio site with brand projects, other photos, and more where the front end React.js app in `client` will serve as most of the website (hosted on Hostinger), though `server`  (hosted on Cyclic) is called by client to respond with the image contents in jasiahpowers.com/photos. all the server is doing here is calling to cloudinary api*
***components*** 

- *HomePage*:
    - top left soundcloud redirect
    - top right mailto: link
    - hero section (wrapped in theme colored shadow) (soon to be its own jsx):
        - full width youtube *iframe*
        - left column buttons aligned left:
            - projects (*ProjectsPage*)
            - prints (redirect)
        - right column buttons aligned right:
            - photos (*PhotosPage*)
            - video (*VideoPage*)
    - *Footer*

- *ProjectsPage*:
    - *Header*
    - *Card* components for each project, with the title and 6 preview thumbnails
        - each is clickable and will redirect to the project’s respective *ProjectPage*
    - *Footer*

- *PhotosPage*:
    - *Header*
    - fetch images from cloudinary folder with backend and serve them here in a *Masonry* material-ui component, which maximizes space for differing dimensions (
        - *LoadingPage* called until loaded ≥1 photo
        - uses *LazyLoad* to dynamically load on scroll
    - *Footer*

- *VideoPage*:
    - *Header*
    - displays all videos in playlist with the google youtube api
    - *Footer*

- *Header:*
    - far left: *HomePage* redirect
    - far right: redirects to *route* where jasiahpowers.com/*route*

- *Footer:*
    - instagram, twitter, youtube, tiktok buttons loaded dynamically from custom filenaming {platform}_icon.png
    - “©  JASIAH POWERS 2024”

- *Button:*
    - all of same style: slight pink, no border, darken on hover

- *Card:*
    - slight pink border, light beige background near white
    - usually 4x3 depending on screen size (in responsive grid)zzz
