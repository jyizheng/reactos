
add_executable(winhttp_apitest WinHttpOpen.c testlist.c)
target_link_libraries(winhttp_apitest wine)
set_module_type(winhttp_apitest win32cui)
add_importlibs(winhttp_apitest msvcrt kernel32 ntdll)
#add_delay_importlibs(winhttp_apitest winhttp)
add_cd_file(TARGET winhttp_apitest DESTINATION reactos/bin FOR all)
