cmake_minimum_required(VERSION 3.12)
project(Stockfish)

set(CMAKE_CXX_STANDARD 14)

include_directories(src)
include_directories(src/syzygy)

find_package(Threads)

add_executable(Stockfish
        src/syzygy/tbprobe.cpp
        src/syzygy/tbprobe.h
        src/benchmark.cpp
        src/bitbase.cpp
        src/bitboard.cpp
        src/bitboard.h
        src/endgame.cpp
        src/endgame.h
        src/evaluate.cpp
        src/evaluate.h
        src/main.cpp
        src/material.cpp
        src/material.h
        src/misc.cpp
        src/misc.h
        src/movegen.cpp
        src/movegen.h
        src/movepick.cpp
        src/movepick.h
        src/pawns.cpp
        src/pawns.h
        src/position.cpp
        src/position.h
        src/psqt.cpp
        src/search.cpp
        src/search.h
        src/thread.cpp
        src/thread.h
        src/thread_win32.h
        src/timeman.cpp
        src/timeman.h
        src/tt.cpp
        src/tt.h
        src/types.h
        src/uci.cpp
        src/uci.h
        src/ucioption.cpp)

target_link_libraries(Stockfish Threads::Threads)