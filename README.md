# UnitPlayer TV

**English** | [简体中文](README.zh-CN.md)

Turns an Android TV or TV box into something you can send videos to from your phone.

Open UnitPlayer TV on the TV and it shows up in the cast list of any app that casts over DLNA. Pick it, and the video plays on the TV, full screen, while the phone becomes the remote.

> **Status: first preview (0.1).** It receives and plays. Subtitles sent from the phone, starting by itself in the background, and a library of its own are not there yet.

## What it does

- **Receives videos over DLNA** from phones and computers on the same network. It was made to go with UnitPlayer for Android (its "Play on a TV" button), and works with other DLNA senders too.
- **Plays them full screen**: MP4, MKV, WebM, MOV, TS, HLS streams and whatever else the TV's own decoders handle.
- **The TV remote works**: OK plays or pauses, left and right go 10 seconds back or forward, Back stops.
- **The phone stays in control**: pause, seek, the TV's volume, and where the video has got to.
- **Nothing else**: no account, no ads, nothing collected. It reads the one address it's sent and that's all it does on the network.

## Install

UnitPlayer TV isn't in an app store. Download the `.apk` from [Releases](../../releases/latest) and install it on the TV one of these ways:

- **From a USB stick**: copy the file onto it, plug it into the TV and open it with the TV's file manager. The TV asks once whether to allow installing from there.
- **With adb**, from a computer on the same network (turn on "Network debugging" in the TV's developer options first):

  ```sh
  adb connect <the TV's address>
  adb install UnitPlayerTV-0.1-1.apk
  ```

Android 8.0 or later. Tested on an Android TV 12 television.

To check the download: the SHA-256 of `UnitPlayerTV-0.1-1.apk` is
`daa416b89c38d1c3e6ee757d0e23dfb39d8fb6708b482ca2ffa9cac9583293b7`.

## Use

1. Open **UnitPlayer TV** on the TV. It says "Ready to play" and the name it goes by.
2. On the phone, open a video and choose the cast button, then that name.
3. Leave the app open on the TV while you watch: it listens only while it's on screen.

The phone and the TV need to be on the same network.

## Good to know

- **Subtitles** picked on the phone don't arrive yet.
- **It has to be open** to be found. Switching to another app on the TV stops it.
- What plays depends on the TV: a format the TV can't decode shows "This video can't be played here".

## Feedback

Problems and ideas: [open an issue](../../issues).

The app is free to use. Its source isn't published.
