Exec Trace
==========

On linux we can trace exec() syscalls using strace. But there no strace for MacOS.
So we must use dtrace and some hacks....
Note: This methood not perfectly correct. Because of kennel limitation we must read parameters from application stack, but when system process dtrace buffer, stack may be already changed. Also dtrace buffers can be dropped.
