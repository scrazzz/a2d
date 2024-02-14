<h1 align="center"> <code>Archive2Discord</code> </h1>
<h4 align="center"> Archive your favourite 4Chan thread 2 Discord before it gets deleted</h4>

[a2d_demo.mp4](https://user-images.githubusercontent.com/70033559/230702359-7722cf06-8ab0-457b-8ae0-44c017f5deb4.mp4)

## Install
Install using pip:
```console
pip install -U a2d
```

## Usage

### Required URLs
First, you'll need the URL of the thread you want to archive (e.g: https://boards.4chan.org/wg/thread/7977599). After that, [create a Discord webhook](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks) and copy the URL.

### CLI arguments
```console
Usage: a2d [OPTIONS] THREAD WEBHOOK
```
The first agument should be the thread URL and the second argument should be the webhook URL.

If you want to archive the entire thread:
```console
a2d https://boards.4chan.org/wg/thread/7977599 https://discord.com/api/webhooks/1093195001258836058/xxxxx
```

### CLI options
There's some options to customize on what you want to archive. Here are the ones that are implemented:

#### `--skip-comments`
Using this flag skips all comments and only archives attachments.
> **Note**
> Does not skip comments WITH attachments.
```console
a2d thread_url webhook_url --skip-comments
```

#### `skip-files`
Using this flag skips all comments with attachment and only archives comments.
```console
a2d thread_url webhook_url --skip-files
```

#### `--delay INTEGER`
Use this to set a delay when archiving to Discord
```console
a2d thread_url webhook_url --delay 5
```
