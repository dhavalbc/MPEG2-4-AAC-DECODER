Modified latm aac decoder based on open source python decoder written by Arkq.
https://gist.github.com/Arkq/66fe948c1051684d8909d730c34396d8

This decoder will decode AAC audio(IOS devices) captured with FTS HCI A2DP dump and save it in a playable audio WAV format.

Please check the following steps to use the same on windows or linux

1. Install latest python version > 3 on either windows or linux.

2. Download ffmpeg binaries from following link
https://ffmpeg.zeranoe.com/builds/

3. Extract the ffmpeg binaries and add the extracted bin folder to system path, for linux it can be done by exporting PATH variable
and for windows it can be done by changing environment path variable.

4. Install pydub using following command
pip install pydub

5. Extract LATM AAC audio from FTS by following below steps
    a) view -> extract audio -> select a2dp -> extract -> save.
    
6. To decode the latm mpeg2,4 aac audio run following command with the attached python script.
      latm_aac_decoder.py <extracted latm mpeg2,4 aac audio>
eg :  latm_aac_decoder.py Bookmarked_snoop(A2DP)(1).mpeg24

7. On successful decode playable wav file should be generated in following format.
<extracted latm mpeg2,4 aac audio>.wav
eg : Bookmarked_snoop(A2DP)(1).wav

If the aac audio bit stream is encoded with 48khz sampling rate, same can be specified using following command line option
latm_aac_decoder.py <extracted latm mpeg2,4 aac audio> 48khz
