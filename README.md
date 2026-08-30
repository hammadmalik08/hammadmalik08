
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">

    <!-- Mobile Responsive -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Instagram Clone</title>

    <style>
        /* =========================
           RESET
        ========================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background: #fafafa;
            color: #111;
        }

        /* =========================
           MAIN LAYOUT
        ========================== */
        .content {
            min-height: 100vh;
            display: flex;
        }

        /* =========================
           SIDEBAR
        ========================== */
        .sidebar {
            width: 245px;
            min-height: 100vh;
            border-right: 1px solid #dbdbdb;
            padding: 30px 20px;
            background: white;
            position: fixed;
            top: 0;
            left: 0;
        }

        .logo {
            font-size: 28px;
            margin-bottom: 40px;
            font-family: cursive;
        }

        .menu {
            list-style: auto;
        }

        .menu li {
            display: flex;
            align-items: center;
            gap: 16px;
            margin: 12px 0;
            padding: 12px;
            font-size: 17px;
            cursor: pointer;
            border-radius: 10px;
            transition: 0.3s;
        }

        .menu li:hover {
            background: #f2f2f2;
        }

        .icon {
            width: 24px;
            height: 24px;
            object-fit: contain;
        }

        /* =========================
           CENTER FEED
        ========================== */
        .feed {
            width: 630px;
            margin-left: 270px;
            padding: 30px 20px;
        }

        /* =========================
           STORIES
        ========================== */
        .stories {
            display: flex;
            gap: 15px;
            overflow-x: auto;
            padding: 10px 5px 20px;
            margin-bottom: 20px;
            scrollbar-width: none;
        }

        .stories::-webkit-scrollbar {
            display: auto;
        }

        .story {
            flex-shrink: 0;
            text-align: center;
            font-size: 12px;
        }

        .boy {
            width: 68px;
            height: 68px;
            border-radius: 50%;
            border: 3px solid #e1306c;
            padding: 2px;
            object-fit: cover;
            display: block;
            margin-bottom: 5px;
        }

        /* =========================
           POST
        ========================== */
        .post {
            width: 100%;
            background: white;
            border: 1px solid #dbdbdb;
            border-radius: 8px;
            overflow: hidden;
            margin-bottom: 25px;
        }

        .posthead {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 12px;
        }

        .imran {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            object-fit: cover;
            border: 2px solid #e1306c;
        }

        .username {
            font-size: 15px;
            font-weight: bold;
        }

        .post-image {
            width: 100%;
            height: 420px;
            object-fit: cover;
            display: block;
        }

        /* =========================
           POST ACTIONS
        ========================== */
        .post-actions {
            display: flex;
            align-items: center;
            padding: 12px;
            gap: 15px;
        }

        .img-icon,
        .icon-img {
            width: 28px;
            height: 28px;
            object-fit: contain;
            cursor: pointer;
            transition: 0.2s;
        }

        .img-icon:hover,
        .icon-img:hover {
            transform: scale(1.1);
        }

        .save-icon {
            margin-left: auto;
        }

        .caption {
            padding: 0 12px 15px;
            font-size: 15px;
            line-height: 1.5;
        }

        /* =========================
           RIGHT SIDEBAR
        ========================== */
        .right-sidebar {
            width: 300px;
            padding: 40px 20px;
            margin-left: 20px;
        }

        .profile-row,
        .suggestion {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 20px;
        }

        .right-img {
            width: 48px;
            height: 48px;
            border-radius: 50%;
            object-fit: cover;
        }

        .profile-name {
            font-size: 20px;
        }
        .suggest-title {
            color: #777;
            font-size: 15px;
            margin-bottom: 20px;
            font-weight: bold;
        }

        .suggestion h3 {
            font-size: 18px;
        }

        /* =========================
           TABLET RESPONSIVE
        ========================== */
        @media (max-width: 1100px) {

            .right-sidebar {
                display: auto;
            }

            .feed {
                margin-left: auto;
                margin-right: auto;
            }
        }

        /* =========================
           MOBILE / ANDROID / IOS
        ========================== */
        @media (max-width: 768px) {

            body {
                padding-bottom: 70px;
            }

            .sidebar {
                width: 100%;
                height: 65px;
                min-height: auto;
                position: fixed;
                top: auto;
                bottom: 0;
                left: 0;
                z-index: 1000;
                padding: 5px 10px;
                border-top: 1px solid #dbdbdb;
                border-right: none;
                display: flex;
                align-items: center;
                justify-content: center;
            }

            .logo {
                display: none;
            }

            .menu {
                width: 100%;
                display: flex;
                align-items: center;
                justify-content: space-around;
            }

            .menu li {
                margin: 0;
                padding: 8px;
                gap: 0;
            }

            .menu li span {
                display: none;
            }

            .icon {
                width: 25px;
                height: 25px;
            }

            .feed {
                width: 100%;
                margin: 0;
                padding: 10px 0;
            }

            .stories {
                padding-left: 15px;
                gap: 15px;
                border-bottom: 3px solid #dbdbdb;
                margin-bottom: 10px;
            }

            .boy {
                width: 62px;
                height: 62px;
            }

            .post {
                border-left: none;
                border-right: none;
                border-radius: 0;
                margin-bottom: 12px;
            }

            .post-image {
                height: auto;
                max-height: 500px;
                object-fit: cover;
            }

            .right-sidebar {
                display: auto;
            }
        }

        /* =========================
           SMALL MOBILE
        ========================== */
        @media (max-width: 400px) {

            .boy {
                width: 56px;
                height: 56px;
            }

            .stories {
                gap: 20px;
            }

            .posthead {
                padding: 10px;
            }

            .post-actions {
                gap: 12px;
            }

            .img-icon,
            .icon-img {
                width: 25px;
                height: 25px;
            }
        }

    </style>
</head>

<body>

    <div class="content">

        <!-- =========================
             LEFT SIDEBAR
        ========================== -->

        <aside class="sidebar">

            <h2 class="logo">Instagram</h2>

            <ul class="menu">

                <li>
                    <img src="https://cdn-icons-png.flaticon.com/512/25/25694.png" class="icon" alt="Home">
                    <span>Home</span>
                </li>

                <li>
                    <img src="https://cdn-icons-png.flaticon.com/512/54/54481.png" class="icon" alt="Search">
                    <span>Search</span>
                </li>

                <li>
                    <img src="https://cdn-icons-png.flaticon.com/512/149/149852.png" class="icon" alt="Explore">
                    <span>Explore</span>
                </li>

                <li>
                    <img src="https://cdn-icons-png.flaticon.com/512/134/134914.png" class="icon" alt="Messages">
                    <span>Messages</span>
                </li>

                <li>
                    <img src="https://cdn-icons-png.flaticon.com/512/1827/1827349.png" class="icon" alt="Notifications">
                    <span>Notifications</span>
                </li>

                <li>
                    <img src="https://cdn-icons-png.flaticon.com/512/1828/1828925.png" class="icon" alt="Create">
                    <span>Create</span>
                </li>

                <li>
                    <img src="https://cdn-icons-png.flaticon.com/512/1077/1077114.png" class="icon" alt="Profile">
                    <span>Profile</span>
                </li>

            </ul>

        </aside>


        <!-- =========================
             MAIN FEED
        ========================== -->

        <main class="feed">


            <!-- STORIES -->

            <div class="stories">

                <div class="story">
                    <img class="boy"
                        src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?auto=format&fit=crop&w=200&q=80"
                        alt="Story">
                    Hammad
                </div>

                <div class="story">
                    <img class="boy"
                        src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?auto=format&fit=crop&w=200&q=80"
                        alt="Story">
                    Ali
                </div>

                <div class="story">
                    <img class="boy"
                        src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?auto=format&fit=crop&w=200&q=80"
                        alt="Story">
                    Sara
                </div>

                <div class="story">
                    <img class="boy"
                        src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?auto=format&fit=crop&w=200&q=80"
                        alt="Story">
                    Saad
                </div>

                <div class="story">
                    <img class="boy"
                        src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?auto=format&fit=crop&w=200&q=80"
                        alt="Story">
                    Ayesha
                </div>

                <div class="story">
                    <img class="boy"
                        src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&w=200&q=80"
                        alt="Story">
                    Ahmed
                </div>

            </div>


            <!-- =========================
                 POST
            ========================== -->

            <article class="post">

                <!-- POST HEADER -->

                <div class="posthead">

                    <img class="imran"
                        src="https://images.unsplash.com/photo-1560250097-0b93528c311a?auto=format&fit=crop&w=200&q=80"
                        alt="Profile">

                    <span class="username">Imran Khan</span>

                </div>


                <!-- POST IMAGE -->

                <img class="post-image"
                    src="https://images.unsplash.com/photo-1529107386315-e1a2ed48a620?auto=format&fit=crop&w=1000&q=80"
                    alt="Post Image">


                <!-- ACTION BUTTONS -->

                <div class="post-actions">

                    <img class="img-icon"
                        src="https://cdn-icons-png.flaticon.com/512/1077/1077035.png"
                        alt="Like">

                    <img class="img-icon"
                        src="https://cdn-icons-png.flaticon.com/512/1380/1380338.png"
                        alt="Comment">

                    <img class="img-icon"
                        src="https://cdn-icons-png.flaticon.com/512/929/929468.png"
                        alt="Share">

                    <img class="icon-img save-icon"
                        src="https://cdn-icons-png.flaticon.com/512/5662/5662990.png"
                        alt="Save">

                </div>


                <!-- CAPTION -->

                <div class="caption">

                    <p>
                        <b>calvarymagazine</b>
                        This Is A Leader Of Pakistan 🔥
                    </p>

                </div>

            </article>

        </main>


        <!-- =========================
             RIGHT SIDEBAR
        ========================== -->

        <aside class="right-sidebar">

            <div class="profile-row">

                <img class="right-img"
                    src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?auto=format&fit=crop&w=200&q=80"
                    alt="Profile">

                <h3 class="profile-name">Codewithherry</h3>

            </div>


            <h3 class="suggest-title">Suggestions For You</h3>


            <div class="suggestion">

                <img class="right-img"
                    src="https://images.unsplash.com/photo-1560250097-0b93528c311a?auto=format&fit=crop&w=200&q=80"
                    alt="Imran Khan">

                <h3>Imran Khan</h3>

            </div>


            <div class="suggestion">

                <img class="right-img"
                    src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&w=200&q=80"
                    alt="Saad Hashmi">

                <h3>Saad Hashmi</h3>

            </div>


            <div class="suggestion">

                <img class="right-img"
                    src="https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?auto=format&fit=crop&w=200&q=80"
                    alt="Profile">

                <h3>PPP Official</h3>

            </div>


            <div class="suggestion">

                <img class="right-img"
                    src="https://images.unsplash.com/photo-1551836022-d5d88e9218df?auto=format&fit=crop&w=200&q=80"
                    alt="PTI Official">

                <h3>PTI Official</h3>

            </div>

        </aside>

    </div>

</body>
</html>
