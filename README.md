# neblina - audio fog machine
#### Video Demo:  <URL HERE>
#### Description:
Using pyo library as a sound engine to create an audio effect processor.
Using PyQt6 library to create the GUI.
____________________________

neblina creates two different flavors of reverbs:

'light reverb' - creates harmonic content and a large atmosphere

'fog reverb' - creates a distorted atmosphere

The two reverbs are mixed with the input signal to create a spacious, beautifully distorted atmosphere.

light reverb
- delay1 for smoothness
- delay2 for ambiance and fractals
- chorus for extra color
- reverb for space

fog reverb
- distortion for grit
- dist_delay to make distortion sound longer
- dirt_delay to have the distorted signal repeat
- grimeverb to create a distorted space
____________________________

Challenges
- implementing a way to stream live sound from an external (ob-6) source - DONE
- chaining all the effect together - DONE
- compress the master signal, do not let output exceed -3 db
- implementing a wet/dry feature
- creating a GUI
    - dropdowns for interactive I/O
    - knobs for aggregate functions
    - signal output visualizer and control
    - info bubbles for each widget giving brief explanation
- creating lfos
    - lfo to module shapes of other lfos 
____________________________

IN PROGRESS
- create a GUI for control and aggregate function knobs
    - knobs or faders? - QDial, QSlider
    - display signal level - QProgressBar
        - be able to control
        - displays decibel level, similar to ableton
    - audio I/O - QComboBox for dropdown menu
        - run pa_list_devices() to get a list for inputs and outputs
        - for inputs: regex (r"^(\d*):\s IN,.*$") - gets input number
        - for outputs: regex (r"^(\d*):\s OUT,.*$") - gets output number
    - info bubbles - QLabel
____________________________

TO DO
- create lfos to modulate times in delays,reverbs and chorus
- implement a wet/dry feature
- create aggregate functions
    - input volume control
    - fog (distortion, noise) knob
    - space knob (reverb and delay time)
    - disintegrate (reverb decay)
    - haze (harmonic content - chorus / delay frequency)
    - master lfo controls - speed, amount, shape
    - wet/dry knob
- audio routing
    - implement audio output
    - if one audio output, sum to mono
    - if two audio outputs, output in stereo
    - mix wet and dry signals 
    - create master mix DONE
______________________________

DONE
- customize distortion parameter DONE
- customize delay1 parameter DONE
- customize delay2 parameter DONE
- customize chorus parameter DONE
- customize reverb parameter DONE
- chain everything together, test different signal paths DONE

______________________________
Acknowledgments
- pyo 1.0.4 documentation by AJAX SOUND STUDIO (http://ajaxsoundstudio.com/pyodoc/index.html#)
- PyQt v6.4.1 documentation by River Bank Computing (https://www.riverbankcomputing.com/static/Docs/PyQt6/)
- pythonguis.com PyQt6 tutorials (https://www.pythonguis.com/pyqt6/)