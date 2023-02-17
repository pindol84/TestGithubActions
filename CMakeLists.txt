project(JsonInCmake)

cmake_minimum_required(VERSION 3.25)

file(READ ${CMAKE_CURRENT_SOURCE_DIR}/test.json MY_JSON_STRING)

string(JSON CUR_NAME GET ${MY_JSON_STRING} 0 name)
string(JSON CUR_URL GET ${MY_JSON_STRING} 0 url)
message(STATUS "==> ${CUR_NAME} : ${CUR_URL}")

string(JSON CUR_NAME GET ${MY_JSON_STRING} 1 name)
string(JSON CUR_URL GET ${MY_JSON_STRING} 1 url)
message(STATUS "==> ${CUR_NAME} : ${CUR_URL}")