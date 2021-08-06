This is module was originally part of WebRTC Native module but has been extracted by me and is configured to be built using Cmake.

This module can be built into a static library and be easily integrated into your project.

```
//To build with Visual Studio 
cmake -G "Visual Studio 16 2019
//This will create a Solution which can be used to compile webrtcvad.lib

```

The header file to be included is located in:
> common_audio/vad/include/webrtc_vad.h


Example Usage: 

```C++

    //Initialization
    
    vadModule = WebRtcVad_Create();
    int vaderr = WebRtcVad_Init(vadModule);

    if(vaderr == -1){
        //std::cout << "Failed to intialize VAD module." << std::endl;
        exit(0);
    }

```



```C++

    //Detection

    int voiceDetected = WebRtcVad_Process(vadModule, SampleRate, DecodedData, frame_size);

    if(voiceDetected == 0) {
    
        CurrentlySpeaking = false; //Not currently speaking

    } else if (voiceDetected > 0) {
    
        CurrentlySpeaking = true; //Currently speaking

    }

```
