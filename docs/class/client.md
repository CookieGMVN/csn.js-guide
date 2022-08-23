# CSNClient
The main Client for csn.js

## Constructor
```js
new CSNClient(options);
```

| Parameter | Type                                          | Description                  |
| --------- | --------------------------------------------- | ---------------------------- |
| options   | [ClientOptions](/docs/typedefs/clientoptions) | Options for this client      |

| Methods                               | Properties        |
| ------------------------------------- | ----------------- |
| [getAudioUrl](#getaudiourlsongdata)   | [cookie](#cookie) |
| [search](#searchsearchdata)           |
| [getNextSongs](#getnextsongssongdata) |
| [getVideoUrl](#getvideourlvideodata)  |
| [getTopCharts](#gettopcharts)         |
| [getAlbum](#getalbumalbumdata)        |
| [getLyrics](#getlyricssongdata)       |

## Methods
> ### .getAudioUrl(songData)
Get audio url from a song.
>
| Parameter     | Type                                      | Description |
| ------------- | ----------------------------------------- | ----------- |
| songData      | [SongOptions](/docs/typedefs/songoptions) | Song data   |
**Returns:** [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&#60;[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) &#60;[AudioResponse](/docs/class/audioresponse)&#62;&#62;

> ### .search(searchData)
Search songs, artists, albums and videos from Chiasenhac Search API
>
| Parameter       | Type                                          | Description |
| --------------- | --------------------------------------------- | ----------- |
| searchData      | [SearchOptions](/docs/typedefs/searchoptions) | Search data |
**Returns:** [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&#60;[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) &#60;[SongData](/docs/class/songdata) or [VideoData](/docs/class/videodata) or [ArtistData](/docs/class/artistdata) or [AlbumData](/docs/class/albumdata)&#62;&#62;

> ### .getNextSongs(songData)
Get next songs for current song.
>
| Parameter     | Type                                      | Description |
| ------------- | ----------------------------------------- | ----------- |
| songData      | [SongOptions](/docs/typedefs/songoptions) | Song data   |
**Returns:** [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&#60;[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) &#60;[NextSongResponse](/docs/class/nextsongresponse)&#62;&#62;

> ### .getVideoUrl(videoData)
Get video url from a video.
>
| Parameter      | Type                                         | Description |
| -------------- | -------------------------------------------- | ----------- |
| videoData      | [VideoOptions](/docs/typedefs/videooptions)  | Video data  |
**Returns:** [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&#60;[VideoResponse](/docs/class/videoresponse)&#62;

> ### .getTopCharts()
Get current top charts over the world.
>
**Returns:** [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&#60;[TopChartResponse](/docs/class/topchartresponse)&#62;

> ### .getAlbum(albumData)
Get full song list for of album.
>
| Parameter      | Type                                         | Description |
| -------------- | -------------------------------------------- | ----------- |
| albumData      | [AlbumOptions](/docs/typedefs/albumoptions)  | Album data  |
**Returns:** [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&#60;[AlbumResponse](/docs/class/topchartresponse)&#62;

> ### .getLyrics(songData)
Get lyric for current song.
>
| Parameter     | Type                                      | Description |
| ------------- | ----------------------------------------- | ----------- |
| songData      | [SongOptions](/docs/typedefs/songoptions) | Song data   |
**Returns:** [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

## Properties
> ### .cookie
Get cookie for this client
>
**Type:** [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)&#60;[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)&#62;