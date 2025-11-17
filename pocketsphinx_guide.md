# PocketSphinx Usage Guide

## Quick Start

### 1. Simple Method (using SpeechRecognition)
```bash
python3 pocketsphinx_simple.py
```

### 2. Advanced Method (direct API)
```bash
python3 pocketsphinx_advanced.py
```

### 3. Command Line Usage

#### Listen from microphone:
```bash
pocketsphinx_continuous -inmic yes
```

#### Transcribe audio file:
```bash
pocketsphinx_continuous -infile /path/to/audio.wav
```

#### With custom settings:
```bash
pocketsphinx_continuous -inmic yes -time yes -logfn /dev/null
```

## Key Features

### Advantages:
- ✅ **Completely offline** - no internet required
- ✅ **Fast and lightweight**
- ✅ **Free and open source**
- ✅ **Real-time capable**
- ✅ **Already installed on your system**

### Limitations:
- ❌ Lower accuracy compared to modern neural models
- ❌ Limited vocabulary by default
- ❌ Best with clear, slow speech
- ❌ US English model only (without additional downloads)

## Audio Format Requirements

PocketSphinx works best with:
- **Sample rate**: 16000 Hz (16 kHz)
- **Channels**: Mono (1 channel)
- **Format**: WAV, 16-bit PCM
- **Quality**: Clear audio, minimal background noise

## Improving Accuracy

### 1. Audio Quality
- Use a good microphone
- Record in quiet environment
- Speak clearly and at moderate pace
- Maintain consistent volume

### 2. Custom Vocabulary
You can create custom dictionaries and language models for specific domains:
```bash
# Create custom dictionary
echo "customword K AH S T AH M W ER D" >> custom.dict

# Use with PocketSphinx
pocketsphinx_continuous -inmic yes -dict custom.dict
```

### 3. Noise Reduction
Preprocess audio to reduce background noise before transcription.

## Testing Your Installation

### Test microphone:
```bash
# Test if microphone works
python3 -c "
import pyaudio
p = pyaudio.PyAudio()
print('Available audio devices:')
for i in range(p.get_device_count()):
    info = p.get_device_info_by_index(i)
    if info['maxInputChannels'] > 0:
        print(f'{i}: {info[\"name\"]}')
p.terminate()
"
```

### Test PocketSphinx:
```bash
# Quick test
python3 -c "
import speech_recognition as sr
r = sr.Recognizer()
print('PocketSphinx test successful')
"
```

## Common Issues and Solutions

### 1. "No module named 'pocketsphinx'"
```bash
sudo apt install python3-pocketsphinx
# or
pip install pocketsphinx
```

### 2. "No module named 'pyaudio'"
```bash
sudo apt install python3-pyaudio
# or
pip install pyaudio
```

### 3. Permission denied for microphone
```bash
# Add user to audio group
sudo usermod -a -G audio $USER
# Then logout and login again
```

### 4. Poor transcription quality
- Ensure 16kHz sample rate
- Use mono audio
- Reduce background noise
- Speak clearly and slowly

## Integration Examples

### Save transcription to file:
```python
import speech_recognition as sr

r = sr.Recognizer()
with sr.Microphone() as source:
    audio = r.listen(source)

text = r.recognize_sphinx(audio)
with open('transcription.txt', 'w') as f:
    f.write(text)
```

### Real-time streaming:
```python
# See pocketsphinx_advanced.py for complete example
transcriber = PocketSphinxTranscriber()
result = transcriber.real_time_transcribe(duration=60)
```

## Next Steps

1. **Try the examples**: Run both Python scripts
2. **Test with your voice**: Adjust microphone settings
3. **Experiment with audio files**: Use different formats
4. **Compare with other backends**: Try Whisper or Vosk for comparison
5. **Custom models**: Create domain-specific vocabularies

## Performance Tips

- Use 16kHz audio for best results
- Keep utterances under 10 seconds for real-time processing
- Process audio in chunks for long recordings
- Use VAD (Voice Activity Detection) to reduce processing

