file(GLOB hdrs "*.h*")
file(GLOB srcs "*.cpp")

#include_directories("${CMAKE_CURRENT_SOURCE_DIR}/../3rdparty")

add_executable(${expressiontest} ${srcs} ${hdrs}) #Создаем проект с именем из переменной ${expressiontest}, в него добавляются файлы из переменных ${srcs} и ${hdrs}
target_link_libraries(${expressiontest} ${expressionlib} gtest) #Подключаем к проекту с именем ${expression} библиотеки с именами ${expressionlib} и gtest
