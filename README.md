```kotlin
import java.nio.ByteBuffer
import java.nio.ByteOrder.LITTLE_ENDIAN

fun main() = ByteBuffer
    .allocate(12)
    .order(LITTLE_ENDIAN)
    .putLong(0x206D2749202C6948)
    .putInt(0x746143)
    .put(11, 0xA)
    .array()
    .let(System.out::write)
```
