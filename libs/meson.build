###############################################################################

subdir('lv2-ttl-generator')

juce_dirs = [
    'juce5-gpl2',
    'juce5',
    'juce6.0',
    'juce6.1',
    # NOTICE no plugins imported that use juce7 yet
    'juce7',
]

enabled_juce_dirs = []
foreach i : range(juce_dirs.length())
    if build_only_flags[i]
        enabled_juce_dirs += [juce_dirs[i]]
    endif
endforeach

if enabled_juce_dirs.length() > 1
    enabled_juce_dirs = []
elif enabled_juce_dirs == []
    enabled_juce_dirs = juce_dirs
endif

foreach juce_dir : enabled_juce_dirs
    if juce_dir == 'juce5-gpl2'
        subdir('drowaudio-juce5-gpl2')
    elif juce_dir == 'juce5'
        subdir('drowaudio-juce5')
        subdir('juced')
    endif
    subdir(juce_dir)
endforeach

###############################################################################
