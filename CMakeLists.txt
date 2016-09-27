cmake_minimum_required (VERSION 2.8.11)
project (aws_iot)
add_library(awsiot ${CMAKE_SOURCE_DIR}/src/aws_iot_json_utils.c src/aws_iot_mqtt_client.c src/aws_iot_mqtt_client_common_internal.c src/aws_iot_mqtt_client_connect.c src/aws_iot_mqtt_client_publish.c src/aws_iot_mqtt_client_subscribe.c src/aws_iot_mqtt_client_unsubscribe.c src/aws_iot_mqtt_client_yield.c src/aws_iot_shadow.c src/aws_iot_shadow_actions.c src/aws_iot_shadow_json.c src/aws_iot_shadow_records.c)
target_include_directories(awsiot PUBLIC ${CMAKE_SOURCE_DIR}/include ${CMAKE_SOURCE_DIR}/external_libs/jsmn ${CMAKE_SOURCE_DIR}/platform/linux/common ${CMAKE_SOURCE_DIR}/platform/linux/mbedtls)


