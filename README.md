ngx_openresty_lua_leveldb
=========================

 - ngx_openresty_lua_leveldb
 - leveldb.lua   put into the path: your openresty/lualib/resty/
 - test.lua     nginx 调用
 
 -location /leveldb {
 -default_type 'application/json';
 -content_by_lua_file conf/lua/test.lua;
 -lua_code_cache on;
 -}
 - leveldb version 1.15.0
 - cd leveldb/include/leveldb/
 - gcc -P -E c.h 生成lua type def  
