# Wyoming Add-ons

Docker-only builds for Home Assistant add-ons that use the [Wyoming protocol](https://github.com/rhasspy/rhasspy3/blob/master/docs/wyoming.md), specifically:

* [Whisper](https://hub.docker.com/r/rhasspy/wyoming-whisper) ([Add-on](https://github.com/home-assistant/addons/blob/master/whisper/README.md))
* [Piper](https://hub.docker.com/r/rhasspy/wyoming-piper) ([Add-on](https://github.com/home-assistant/addons/blob/master/piper/README.md))
* [openWakeWord](https://hub.docker.com/r/rhasspy/wyoming-openwakeword) ([Add-on](https://github.com/home-assistant/addons/blob/master/openwakeword/README.md))


## Run Whisper

``` sh
docker run -it -p 10300:10300 -v /path/to/local/data:/data rhasspy/wyoming-whisper --model tiny-int8 --language en
```


## Run Piper

``` sh
docker run -it -p 10200:10200 -v /path/to/local/data:/data rhasspy/wyoming-piper --voice en_US-lessac-medium
```

## Run openWakeWord

``` sh
docker run -it -p 10400:10400 rhasspy/wyoming-openwakeword --preload-model 'ok_nabu'
```
