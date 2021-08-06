cmake_minimum_required(VERSION 3.10)

# set the project name
project(webrtcvad)
include_directories(${PROJECT_SOURCE_DIR})

add_definitions(-DWEBRTC_WIN)

# add the executable
add_library(webrtcvad STATIC

${PROJECT_SOURCE_DIR}/common_audio/signal_processing/auto_correlation.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/auto_corr_to_refl_coef.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/complex_bit_reverse.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/complex_fft.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/copy_set_operations.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/cross_correlation.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/division_operations.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/dot_product_with_scale.cc
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/dot_product_with_scale.h
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/downsample_fast.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/energy.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/filter_ar.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/filter_ar_fast_q12.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/filter_ma_fast_q12.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/get_hanning_window.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/get_scaling_square.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/ilbc_specific_functions.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/levinson_durbin.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/lpc_to_refl_coef.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/min_max_operations.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/randomization_functions.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/real_fft.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/refl_coef_to_lpc.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/resample.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/resample_48khz.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/resample_by_2.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/resample_by_2_internal.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/resample_fractional.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/splitting_filter.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/spl_init.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/spl_inl.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/spl_sqrt.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/sqrt_of_one_minus_x_squared.c
${PROJECT_SOURCE_DIR}/common_audio/signal_processing/vector_scaling_operations.c
${PROJECT_SOURCE_DIR}/rtc_base/checks.cc
${PROJECT_SOURCE_DIR}/common_audio/vad/vad_filterbank.c
${PROJECT_SOURCE_DIR}/common_audio/vad/vad_gmm.c
${PROJECT_SOURCE_DIR}/common_audio/vad/vad_sp.c
${PROJECT_SOURCE_DIR}/common_audio/vad/vad_core.c
${PROJECT_SOURCE_DIR}/common_audio/vad/vad.cc
${PROJECT_SOURCE_DIR}/common_audio/vad/webrtc_vad.c 

)

