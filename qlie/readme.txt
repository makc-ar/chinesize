月に寄りそう乙女の作法２
修改：
由于HashVer 版本变化，
  HASHHDR*       hashhdr    = (HASHHDR*) p;
  unsigned char* hash_bytes = p + sizeof(*hashhdr) + hashhdr->length + 36;
  unsigned long  seed       = crc_or_something(hash_bytes, 256) & 0x0FFFFFFF;

此处的 + 36需要改为 + 72
已在exfp31中patch。