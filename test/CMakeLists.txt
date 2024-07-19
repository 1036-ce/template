find_package(GTest REQUIRED)

if (!GTest_FOUNDED) 
	message(FATAL "GTest not found")
endif()

add_executable(jtest test.cpp)

target_link_libraries(jtest
	PRIVATE
		GTest::GTest)

add_test(a jtest)

