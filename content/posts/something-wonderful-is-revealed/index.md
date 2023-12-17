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
{{< grid_words text="Entry for Curtis Holt's render challenge.">}}

<video id="hoverVideo" style="width: 300px; height: 300px;" muted>
    <source src=loopy.mp4>
</video>

<script>
    // Get the video element
    const video = document.getElementById('hoverVideo');

    // Flag to track whether the video is currently playing
    let isPlaying = false;

    // Function to play the video for a specified duration
    function playVideo() {
        // Check if the video is already playing
        if (!isPlaying) {
            // Play the video
            video.play();

            // Set a timeout to pause the video after 1700 ms
            setTimeout(() => {
                // Pause the video if it's not looping
                if (!video.loop) {
                    video.pause();
                    isPlaying = false;
                }
            }, 1700);

            // Update the flag
            isPlaying = true;
        }
    }

    // Add event listener for hover events
    video.addEventListener('mouseenter', playVideo);

    // Add a timeupdate event listener to detect when the video reaches the end
    video.addEventListener('timeupdate', () => {
        // Check if the video is at the end
        if (video.currentTime === video.duration && !video.loop) {
            isPlaying = false;
        }
    });
</script>

{{< /wrap >}}



