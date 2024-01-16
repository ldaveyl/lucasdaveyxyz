---
title: "Something Wonderful is Revealed"
subtitle: ""
draft: false
date: "2023-12-09T20:09:45+01:00"
thumbnail: "thumbnail.png"
---
{{< wrap >}}
{{< youtube id="kDzR4-NJG7A" >}}
{{< break >}}
{{< grid_words text="An animation made for the prompt \"Something wondeful is revealed\".">}}

<video id="clickVideo" style="width: 300px; height: 300px;" loop muted playsinline>
    <source src=0079-0143.mp4>
</video>

<script>
    // Get the video element
    const video = document.getElementById('clickVideo');

    // Flag to track whether the video is currently playing
    let isPlaying = false;

    // Flag to track whether the bunny is showing
    let isOpen = false;

    // Function to play the video for a specified duration
    function playVideo() {

        // Check if the video is already playing
        if (!isPlaying) {

            // Play the video
            video.play();
            console.log("Started video at: " + video.currentTime);

            // Update the flag
            isPlaying = true;
        }
    }

    // Add event listener for click events
    video.addEventListener('click', playVideo);

    // Add a timeupdate event listener to detect when the video reaches the end
    video.addEventListener('timeupdate', () => {

        console.log(video.currentTime);

        if (!isOpen && video.currentTime >= 1.7) {
            video.pause();
            isPlaying = false;
            isOpen = true;
            video.currentTime = 1.7;
        } else if (isOpen && video.currentTime >= 1.95) {
            video.pause();
            isPlaying = false;
            isOpen = false;
            video.currentTime = 0;
        }
    });
</script>
{{< /wrap >}}
