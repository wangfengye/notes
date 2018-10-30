### Question:
> A problem occurred configuring project ':demo'.
07:59:00.932 [ERROR] [org.gradle.internal.buildevents.BuildExceptionReporter] > Could not resolve all dependencies for configuration ':demo:_debugApk'.
07:59:00.932 [ERROR] [org.gradle.internal.buildevents.BuildExceptionReporter]    > A problem occurred configuring project ':FloatingViewLib'.
07:59:00.932 [ERROR] [org.gradle.internal.buildevents.BuildExceptionReporter]       > Failed to notify project evaluation listener.
07:59:00.933 [ERROR] [org.gradle.internal.buildevents.BuildExceptionReporter]          > com.android.build.gradle.tasks.factory.AndroidJavaCompile.setDependencyCacheDir(Ljava/io/File;)V

Solve: gradle版本与 gradle tool版本不对应[查看版本对应关系](https://developer.android.google.cn/studio/releases/gradle-plugin#3-2-0)
