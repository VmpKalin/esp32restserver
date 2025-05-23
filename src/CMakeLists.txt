idf_component_register(SRCS "esp_rest_main.c"
                            "rest_server.c"
                    PRIV_REQUIRES esp_http_server esp_driver_gpio fatfs json spiffs nvs_flash
                    INCLUDE_DIRS ".")