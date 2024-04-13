# Run VLC in the Browser

Quickstart:

```
git clone https://github.com/Krowemoh/vlc.js.git
```

## Example

This is an example of playing a video directly in the browser using VLC.

```
<div>
    <canvas id="canvas" style="background-color:gray;"></canvas>
    <div>
        <button id="play">Play</button>
        <button id="pause">Stop</button>
        <meter id="seekbar" max="100" style="width: 500px" value="0"></meter>
        <meter id="volume" max="100" style="width: 100px" value="80"></meter>
    </div>
</div>

<script src="./lib/vlc/experimental.js"></script>
<script type="module">
    import { VLCPlayer } from "./lib/vlc/vlc.js";

    let video = {
        source: "/path/to/video.mkv"
        options:"--codec=webcodec --aout=emworklet_audio -vv --input-repeat=10000",
        size: { 
            width: "700px", 
            height: "" 
        },
    };

    window.onload = async function () {
        await VLCPlayer(video);
    };
</script>
```

## References

A working demo can be found on the VLC site:

https://videolabs.io/communication/vlcjs-demo/vlc.html


