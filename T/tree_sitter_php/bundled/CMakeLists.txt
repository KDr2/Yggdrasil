cmake_minimum_required(VERSION 3.13)
project(treesitter_php)
set(CMAKE_C_STANDARD 99)

include_directories(tree-sitter/src)
add_library(treesitter_php SHARED tree-sitter/src/parser.c tree-sitter/src/scanner.cc)

install(TARGETS treesitter_php DESTINATION lib CONFIGURATIONS Release)
