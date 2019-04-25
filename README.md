```
* 현재 유튜브 링크 정규식에 맞는 pytube 사용함 
(원본 repository : https://github.com/clianor/voice-speaker-tensorflow/tree/master/ 를 수정함) 
: updated 2018-12-21
```
```
* 현재 유튜브 링크 정규식에 맞는 pytube업데이트 방법: pip install pytube후 extract.py를 다음과 같이 수정 
: updated 2019-04-25

CODE extract.py]

else:
        # I'm not entirely sure what ``t`` represents. Looks to represent a
        # boolean.
        #t = regex_search(
        #    r'\W[\'"]?t[\'"]?: ?[\'"](.+?)[\'"]', watch_html,
        #    group=0,
        #)
        params = OrderedDict([
            ('video_id', video_id),
            ('el', '$el'),
            ('ps', 'default'),
            ('eurl', quote(watch_url)),
            ('hl', 'en_US'),
            #('t', quote(t)),
        ])
```

* * *

### 1. 데이터 수집 및 음성 추출.
download 디렉토리에 유튜브 영상을 수집하는 프로그램이 있습니다.<br>
영상을 수집하고 오디오를 추출하여 wav파일로 뽑아내는 코드도 있습니다.<br>
[이동](https://github.com/gusrud1103/voice_extract_slicing_hk/tree/master/download)

* * *

### 2. 음성 자르기.
추출한 음성 파일을 잘라 추출하는 프로그램이 있습니다.(현재 코드는 10초 간격 단위 슬라이싱)<br>
[이동](https://github.com/gusrud1103/voice_extract_slicing_hk/tree/master/download/audios)

* * *
