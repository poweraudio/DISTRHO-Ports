###############################################################################

lib_drowaudio_juce5_gpl2 = static_library('drowaudio-juce-gpl2',
    sources: [
        '../drowaudio/source/dRowAudio/dRowAudio.cpp'
    ],
    include_directories: [
        include_directories('../drowaudio'),
        include_directories('../juce5-gpl2'),
        include_directories('../juce5-gpl2/source'),
        include_directories('../juce5-gpl2/source/modules'),
    ],
    cpp_args: build_flags_cpp,
    dependencies: dependencies,
    pic: true,
    install: false,
)

###############################################################################
