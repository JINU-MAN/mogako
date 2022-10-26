모각코
---------
#### 모각코 1주차
>모바일 프로그래밍 조별과제의 개발목표와 역할 분담을 위한 회의를 했다. FFT라이브러리를 이용해 고속 푸리에 변환을 통한 기타 튜너를 만들기로 하였다.
>우선은 기타 튜너의 핵심적인 기능인 튜닝 기능과 부가적으로 메트로놈 기능을 개발하고 추가적인 기능들은 기본적인 어플 기능 개발을 한 후에 정하기로 했다.
>역할 분담은 개발(2), 기획(1), 그래픽(1), UI(1)로 분담하였고 나는 개발 중 개발 보조를 담당하게 되었다. 실력이 조금 부족해서 팀에 민폐를 끼치지 않으려면
>추가적인 공부가 필수적일 것 같다.
***
#### 모각코 2주차
>모바일 프로그래밍 팀 프로젝트를 위한 역할 분담 세부사항과 앞으로의 일정 회의를 했다.    항상 과제나 문제만 풀다가 개발을 하려고 하니 잘할 수 있을지 걱정이 된다.
>     그리고 FFT 라이브러리를 사용하기 위해 소리 데이터를 입력 받을 AudioRecord 함수를 공부했다.
>     public AudioRecord(int audioSource, int sampleRateInHz, int channelConfig, int audioFormat, int bufferSizeInBytes)
>     AudioRecord의 생성자를 보면 인자를 5개 받는다는 것을 알 수 있다.
>     첫 번째 인자는 어떤 소리 데이터를 사용할 것인지에 대한 인자로 마이크로 입력받기 위해서는 1을 넣어주면 된다.
>     두 번째 인자는 초당 몇개의 sample을 추출할 것인지에 대한 인자로 값이 커질수록 고음질이 된다. 우리는 음질이 좋을 필요가 없으니 낮은 값을 사용해도 될 것 같다.
>     세 번째 인자인 channel값은 mono/streo 중 선택하는 데 우리는 입체적인 음향이 필요 없으니 mono를 넣으면 될 것 같다.
>     네 번째 인자는 FFT 라이브러리에서 PCM데이터가 필요하므로  AudioFormat.ENCODING_PCM_16BIT를 넣는다.
>     다섯 번째 인자는 한번에 전달 받을 audio data 의 크기를 나타내고, 보통은 AudioRecord 의 getMinBufferSize 함수를 호출해서 return 되는 값으로 지정한다고 한다.
***
#### 모각코 3주차
>컴퓨터 구조 스터디를 했다. instruction으로부터의 입력값이 달라짐에 따라 control회로에서 어떤 output이 나오는지에 관해 공부했다.
>R타입의 경우 op코드가 000000이고 [5-0] funct의 값에 따라 ALUcontrol에서 ALU회로에서 어떤 동작을 해야할지 알려준다.
>add의 경우 ALUcontrol의 값이 0010, sub는 0110 and는 0000 or은 0001 slt는 0111이다
>lw인스트럭션의 경우 op코드가 100011이고 funct의 값은 신경쓰지 않는다 ALUcontrol은 add와 동일하게 0010이다.
>sw인스트럭션은 op코드가 101011인 것만 제외하면 lw인스트럭션의 경우와 같다.
>beq인스트럭션의 op코드는 000100이고 funct의 값은 신경쓰지 않고 ALUcontrol의 값은 0110이다.
***
#### 모각코 4주차
>모바일 프로그래밍 개인과제에서 회원가입과 로그인을 위한 정보를 저장하는 preference에 대해 공부했다.
>프레퍼런스는 회원가입과 로그인 등 데이터의 양이 많이 필요하지 않은 간단한 작업에 적합하다.
>getSharedPreferences()로 선언하고 데이터를 저장/편집하기 위한 Editor변수를 SharedPreferences.Editor editor(에디터 이름)로 선언한다
>데이터를 저장할떄는 editor.put자료형(key,value)로 key값에 value를 저장하고 editor.commit()으로 파일에 저장한다
>불러올떄는 preference이름.get자료형(key,"")로 value값을 불러온다.
