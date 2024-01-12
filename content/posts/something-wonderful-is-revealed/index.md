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

            // Update the flag
            isPlaying = true;
        }
    }

    // Add event listener for click events
    video.addEventListener('click', playVideo);

    // Add a timeupdate event listener to detect when the video reaches the end
    video.addEventListener('timeupdate', () => {
        if (!isOpen && video.currentTime >= 1.7) {
            isPlaying = false;
            isOpen = true;
            video.pause();
        } else if (isOpen && video.currentTime >= 2.1) {
            isPlaying = false;
            isOpen = false;
            video.pause();
            video.currentTime = 0;
        }
    });
</script>
{{< /wrap >}}
