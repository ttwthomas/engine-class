## Launch dashboard
```python3 -m http.server 8000```

Go to http://localhost:8000/index.html  
Accept microphone access  
Click start and play motor sounds


# Things to know
- there is 3 categories:
    - `background`
    - `motor-on`
    - `other`

- It seems like its easier to separate background noise from other sounds (less false positive)
- Confidence score is from 0 to 1
- `motor-timer` is the total time motor sounds has been detected in seconds
- The model makes prediction every 500ms on the last 1sec of sound (`overlapFactor`: 0.50)
- you can play with `consecutive` to wait X consecutive detection to count motor ON
- you can play with `threshold` to detect motor on only if model is X% sure 
- `initializeSprectrogram()` can be safely removed
