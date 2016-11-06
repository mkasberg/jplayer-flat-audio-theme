# jPlayer Flat Audio Theme

A simple jPlayer theme for playing a single audio file.

## Quick Start

1. Install jPlayer on your site. This theme is audio-only, so you can follow the
audio-only [quick start instructions](http://jplayer.org/latest/quick-start-guide/)
if doing this for the first time. Here's a quick summary:
  1. Download [jPlayer](https://github.com/happyworm/jPlayer/releases).
  2. Upload jquery.jplayer.min.js and jquery.jplayer.swf to `/js`.
  3. Include jQuery and jPlayer:

    ```html
    <script type="text/javascript" src="/js/jquery.jplayer.min.js"></script>
    <script type="text/javascript" src="http://code.jquery.com/jquery-1.11.1.min.js"></script>
    ```

2. Our theme requires Font Awesome. Include it. You can do this from the CDN or your own hosted version.

    ```html
    <link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet" integrity="sha384-wvfXpqpZZVQGK6TAh5PVlGOfQNHSoD2xbE+QkPxCAFlNEevoEH3Sl0sibVcOQVnN" crossorigin="anonymous">
    ```

3. Use the CSS for our theme. This is the theme itself, which you can find in the `css` folder of this repository.

    ```html
    <link rel="stylesheet" type="text/css" href="css/jplayer-flat-audio-theme.css" />
    ```

4. Add required HTML. Thel elements here should match what's in our theme.

    ```html
    <div id="jquery_jplayer_1" class="jp-jplayer"></div>
    <div id="jp_container_1" class="jp-audio" role="application" aria-label="media player">
        <div class="jp-type-single">
            <div class="jp-gui jp-interface">
                <div class="jp-controls">
                    <a class="jp-play"><i class="fa fa-play"></i></a>
                    <a class="jp-pause"><i class="fa fa-pause"></i></a>
                    <a class="jp-stop"><i class="fa fa-stop"></i></a>
                </div>
                <div class="jp-progress">
                    <div class="jp-seek-bar">
                        <div class="jp-play-bar"></div>
                    </div>
                </div>
                <div class="jp-volume-controls">
                    <a class="jp-mute"><i class="fa fa-volume-off"></i></a>
                    <a class="jp-volume-max"><i class="fa fa-volume-up"></i></a>
                    <div class="jp-volume-bar">
                        <div class="jp-volume-bar-value"></div>
                    </div>
                </div>
                <div class="jp-time-holder">
                    <div class="jp-current-time" role="timer" aria-label="time">&nbsp;</div>
                    <div class="jp-duration" role="timer" aria-label="duration">&nbsp;</div>
                </div>
            </div>
            <div class="jp-no-solution">
                <span>Update Required</span>
                To play the media you will need to either update your browser to a recent version or update your <a href="http://get.adobe.com/flashplayer/" target="_blank">Flash plugin</a>.
            </div>
        </div>
    </div>
    ```

5. Add Javascript for jPlayer to run on the page. This is just the normal
jPlayer javascript, the same as is used in jPlayer's quick-start guide.

    ```html
    <script type="text/javascript">
    $(document).ready(function(){
      $("#jquery_jplayer_1").jPlayer({
        ready: function () {
          $(this).jPlayer("setMedia", {
            title: "Bubble",
            m4a: "http://www.jplayer.org/audio/m4a/Miaow-07-Bubble.m4a",
            oga: "http://www.jplayer.org/audio/ogg/Miaow-07-Bubble.ogg"
          });
        },
        cssSelectorAncestor: "#jp_container_1",
        swfPath: "/js",
        supplied: "m4a, oga",
        useStateClassSkin: true,
        autoBlur: false,
        smoothPlayBar: true,
        keyEnabled: true,
        remainingDuration: true,
        toggleDuration: true
      });
    });
  </script>
    ```

That's it! You're all set!

## Contributing

Feel free to send a pull request for any improvements.

