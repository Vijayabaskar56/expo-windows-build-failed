Summary
Build Task is Failing Due to Path difference like "" for this Character , sepculating due to difference in the Path Variation on the Windows

Task :app:configureCMakeDebug[arm64-v8a] FAILED
C/C++: CMake Error at E:/Development/apeers-app/node_modules/react-native/ReactAndroid/cmake-utils/ReactNative-application.cmake:42 (add_library):
C/C++: Syntax error in cmake code when parsing string
C/C++: E:\Development\apeers-app\node_modules\react-native\ReactAndroid/cmake-utils/default-app-setup/OnLoad.cpp
C/C++: Invalid character escape '\D'.
C/C++: Call Stack (most recent call first):
C/C++: CMakeLists.txt:31 (include)

FAILURE: Build failed with an exception.

What platform(s) does this occur on?
Android

SDK Version
52

Environment
expo-env-info 1.2.1 environment info:
    System:
      OS: Windows 11 10.0.26100
    Binaries:
      Node: 20.14.0 - C:\Program Files\nodejs\node.EXE
      npm: 10.8.3 - C:\Program Files\nodejs\npm.CMD
    IDEs:
      Android Studio: AI-242.23339.11.2421.12550806
    npmPackages:
      expo: ~52.0.7 => 52.0.7
      expo-router: ~4.0.5 => 4.0.5
      react: 18.3.1 => 18.3.1
      react-dom: 18.3.1 => 18.3.1
      react-native: 0.76.2 => 0.76.2
      react-native-web: ~0.19.13 => 0.19.13
    Expo Workflow: bare
Minimal reproducible example
Here is the Minial Reproduction of the Bug Cointaing Repo

https://github.com/Vijayabaskar56/expo-windows-build-failed.git

Just a Bare new expo application , Failed during Development Build ,

Here is the Full Detailed Log , With

                                              /npm 20.14.0 23:51:37 
➜ bun run android  
$ expo run:android
› Building app...
Configuration on demand is an incubating feature.

> Configure project :expo

Using expo modules
  - expo-asset (11.0.1)
  - expo-blur (14.0.1)
  - expo-constants (17.0.3)
  - expo-file-system (18.0.3)
  - expo-font (13.0.1)
  - expo-haptics (14.0.0)
  - expo-keep-awake (14.0.1)
  - expo-linking (7.0.2)
  - expo-modules-core (2.0.3)
  - expo-splash-screen (0.29.10)
  - expo-system-ui (4.0.3)
  - expo-web-browser (14.0.1)


> Configure project :react-native-reanimated
Android gradle plugin: 8.6.0
Gradle: 8.10.2

> Task :app:configureCMakeDebug[arm64-v8a] FAILED
C/C++: CMake Error at E:/Development/apeers-app/node_modules/react-native/ReactAndroid/cmake-utils/ReactNative-application.cmake:42 (add_library):
C/C++:   Syntax error in cmake code when parsing string
C/C++:     E:\Development\apeers-app\node_modules\react-native\ReactAndroid/cmake-utils/default-app-setup/OnLoad.cpp
C/C++:   Invalid character escape '\D'.
C/C++: Call Stack (most recent call first):
C/C++:   CMakeLists.txt:31 (include)

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:configureCMakeDebug[arm64-v8a]'.
> [CXX1429] error when building with cmake using E:\Development\apeers-app\node_modules\react-native\ReactAndroid\cmake-utils\default-app-setup\CMakeLists.txt: -- The C compiler identification is Clang 17.0.2
  -- The CXX compiler identification is Clang 17.0.2
  -- Detecting C compiler ABI info
  -- Detecting C compiler ABI info - done
  -- Check for working C compiler: C:/Users/vj2k0/AppData/Local/Android/Sdk/ndk/26.1.10909125/toolchains/llvm/prebuilt/windows-x86_64/bin/clang.exe - skipped 
  -- Detecting C compile features
  -- Detecting C compile features - done
  -- Detecting CXX compiler ABI info
  -- Detecting CXX compiler ABI info - done
  -- Check for working CXX compiler: C:/Users/vj2k0/AppData/Local/Android/Sdk/ndk/26.1.10909125/toolchains/llvm/prebuilt/windows-x86_64/bin/clang++.exe - skipped
  -- Detecting CXX compile features
  -- Detecting CXX compile features - done
  -- Configuring incomplete, errors occurred!
  See also "E:/Development/apeers-app/android/app/.cxx/Debug/z2z38611/arm64-v8a/CMakeFiles/CMakeOutput.log".

  C++ build system [configure] failed while executing:
      @echo off
      "C:\\Users\\vj2k0\\AppData\\Local\\Android\\Sdk\\cmake\\3.22.1\\bin\\cmake.exe" ^
        "-HE:\\Development\\apeers-app\\node_modules\\react-native\\ReactAndroid\\cmake-utils\\default-app-setup" ^
        "-DCMAKE_SYSTEM_NAME=Android" ^
        "-DCMAKE_EXPORT_COMPILE_COMMANDS=ON" ^
        "-DCMAKE_SYSTEM_VERSION=24" ^
        "-DANDROID_PLATFORM=android-24" ^
        "-DANDROID_ABI=arm64-v8a" ^
        "-DCMAKE_ANDROID_ARCH_ABI=arm64-v8a" ^
        "-DANDROID_NDK=C:\\Users\\vj2k0\\AppData\\Local\\Android\\Sdk\\ndk\\26.1.10909125" ^
        "-DCMAKE_ANDROID_NDK=C:\\Users\\vj2k0\\AppData\\Local\\Android\\Sdk\\ndk\\26.1.10909125" ^
        "-DCMAKE_TOOLCHAIN_FILE=C:\\Users\\vj2k0\\AppData\\Local\\Android\\Sdk\\ndk\\26.1.10909125\\build\\cmake\\android.toolchain.cmake" ^
        "-DCMAKE_MAKE_PROGRAM=C:\\Users\\vj2k0\\AppData\\Local\\Android\\Sdk\\cmake\\3.22.1\\bin\\ninja.exe" ^
        "-DCMAKE_LIBRARY_OUTPUT_DIRECTORY=E:\\Development\\apeers-app\\android\\app\\build\\intermediates\\cxx\\Debug\\z2z38611\\obj\\arm64-v8a" ^
        "-DCMAKE_RUNTIME_OUTPUT_DIRECTORY=E:\\Development\\apeers-app\\android\\app\\build\\intermediates\\cxx\\Debug\\z2z38611\\obj\\arm64-v8a" ^
        "-DCMAKE_BUILD_TYPE=Debug" ^
        "-DCMAKE_FIND_ROOT_PATH=E:\\Development\\apeers-app\\android\\app\\.cxx\\Debug\\z2z38611\\prefab\\arm64-v8a\\prefab" ^
        "-BE:\\Development\\apeers-app\\android\\app\\.cxx\\Debug\\z2z38611\\arm64-v8a" ^
        -GNinja ^
        "-DPROJECT_BUILD_DIR=E:\\Development\\apeers-app\\android\\app\\build" ^
        "-DREACT_ANDROID_DIR=E:\\Development\\apeers-app\\node_modules\\react-native\\ReactAndroid" ^
        "-DANDROID_STL=c++_shared" ^
        "-DANDROID_USE_LEGACY_TOOLCHAIN_FILE=ON"
    from E:\Development\apeers-app\android\app
  CMake Error at E:/Development/apeers-app/node_modules/react-native/ReactAndroid/cmake-utils/ReactNative-application.cmake:42 (add_library):
    Syntax error in cmake code when parsing string

      E:\Development\apeers-app\node_modules\react-native\ReactAndroid/cmake-utils/default-app-setup/OnLoad.cpp

    Invalid character escape '\D'.
  Call Stack (most recent call first):
    CMakeLists.txt:31 (include) : com.android.ide.common.process.ProcessException: -- The C compiler identification is Clang 17.0.2
  -- The CXX compiler identification is Clang 17.0.2
  -- Detecting C compiler ABI info
  -- Detecting C compiler ABI info - done
  -- Check for working C compiler: C:/Users/vj2k0/AppData/Local/Android/Sdk/ndk/26.1.10909125/toolchains/llvm/prebuilt/windows-x86_64/bin/clang.exe - skipped 
  -- Detecting C compile features
  -- Detecting C compile features - done
  -- Detecting CXX compiler ABI info
  -- Detecting CXX compiler ABI info - done
  -- Check for working CXX compiler: C:/Users/vj2k0/AppData/Local/Android/Sdk/ndk/26.1.10909125/toolchains/llvm/prebuilt/windows-x86_64/bin/clang++.exe - skipped
  -- Detecting CXX compile features
  -- Detecting CXX compile features - done
  -- Configuring incomplete, errors occurred!
  See also "E:/Development/apeers-app/android/app/.cxx/Debug/z2z38611/arm64-v8a/CMakeFiles/CMakeOutput.log".

  C++ build system [configure] failed while executing:
      @echo off
      "C:\\Users\\vj2k0\\AppData\\Local\\Android\\Sdk\\cmake\\3.22.1\\bin\\cmake.exe" ^
        "-HE:\\Development\\apeers-app\\node_modules\\react-native\\ReactAndroid\\cmake-utils\\default-app-setup" ^
        "-DCMAKE_SYSTEM_NAME=Android" ^
        "-DCMAKE_EXPORT_COMPILE_COMMANDS=ON" ^
        "-DCMAKE_SYSTEM_VERSION=24" ^
        "-DANDROID_PLATFORM=android-24" ^
        "-DANDROID_ABI=arm64-v8a" ^
        "-DCMAKE_ANDROID_ARCH_ABI=arm64-v8a" ^
        "-DANDROID_NDK=C:\\Users\\vj2k0\\AppData\\Local\\Android\\Sdk\\ndk\\26.1.10909125" ^
        "-DCMAKE_ANDROID_NDK=C:\\Users\\vj2k0\\AppData\\Local\\Android\\Sdk\\ndk\\26.1.10909125" ^
        "-DCMAKE_TOOLCHAIN_FILE=C:\\Users\\vj2k0\\AppData\\Local\\Android\\Sdk\\ndk\\26.1.10909125\\build\\cmake\\android.toolchain.cmake" ^
        "-DCMAKE_MAKE_PROGRAM=C:\\Users\\vj2k0\\AppData\\Local\\Android\\Sdk\\cmake\\3.22.1\\bin\\ninja.exe" ^
        "-DCMAKE_LIBRARY_OUTPUT_DIRECTORY=E:\\Development\\apeers-app\\android\\app\\build\\intermediates\\cxx\\Debug\\z2z38611\\obj\\arm64-v8a" ^
        "-DCMAKE_RUNTIME_OUTPUT_DIRECTORY=E:\\Development\\apeers-app\\android\\app\\build\\intermediates\\cxx\\Debug\\z2z38611\\obj\\arm64-v8a" ^
        "-DCMAKE_BUILD_TYPE=Debug" ^
        "-DCMAKE_FIND_ROOT_PATH=E:\\Development\\apeers-app\\android\\app\\.cxx\\Debug\\z2z38611\\prefab\\arm64-v8a\\prefab" ^
        "-BE:\\Development\\apeers-app\\android\\app\\.cxx\\Debug\\z2z38611\\arm64-v8a" ^
        -GNinja ^
        "-DPROJECT_BUILD_DIR=E:\\Development\\apeers-app\\android\\app\\build" ^
        "-DREACT_ANDROID_DIR=E:\\Development\\apeers-app\\node_modules\\react-native\\ReactAndroid" ^
        "-DANDROID_STL=c++_shared" ^
        "-DANDROID_USE_LEGACY_TOOLCHAIN_FILE=ON"
    from E:\Development\apeers-app\android\app
  CMake Error at E:/Development/apeers-app/node_modules/react-native/ReactAndroid/cmake-utils/ReactNative-application.cmake:42 (add_library):
    Syntax error in cmake code when parsing string

      E:\Development\apeers-app\node_modules\react-native\ReactAndroid/cmake-utils/default-app-setup/OnLoad.cpp

    Invalid character escape '\D'.
  Call Stack (most recent call first):
    CMakeLists.txt:31 (include)
        at com.android.build.gradle.internal.cxx.process.ExecuteProcessKt.execute(ExecuteProcess.kt:288)
        at com.android.build.gradle.internal.cxx.process.ExecuteProcessKt$executeProcess$1.invoke(ExecuteProcess.kt:108)
        at com.android.build.gradle.internal.cxx.process.ExecuteProcessKt$executeProcess$1.invoke(ExecuteProcess.kt:106)
        at com.android.build.gradle.internal.cxx.timing.TimingEnvironmentKt.time(TimingEnvironment.kt:32)
        at com.android.build.gradle.internal.cxx.process.ExecuteProcessKt.executeProcess(ExecuteProcess.kt:106)
        at com.android.build.gradle.internal.cxx.process.ExecuteProcessKt.executeProcess$default(ExecuteProcess.kt:85)
        at com.android.build.gradle.tasks.CmakeQueryMetadataGenerator.executeProcess(CmakeFileApiMetadataGenerator.kt:59)
        at com.android.build.gradle.tasks.ExternalNativeJsonGenerator$configureOneAbi$1$1$3.invoke(ExternalNativeJsonGenerator.kt:247)
        at com.android.build.gradle.tasks.ExternalNativeJsonGenerator$configureOneAbi$1$1$3.invoke(ExternalNativeJsonGenerator.kt:247)
        at com.android.build.gradle.internal.cxx.timing.TimingEnvironmentKt.time(TimingEnvironment.kt:32)
        at com.android.build.gradle.tasks.ExternalNativeJsonGenerator.configureOneAbi(ExternalNativeJsonGenerator.kt:247)
        at com.android.build.gradle.tasks.ExternalNativeJsonGenerator.configure(ExternalNativeJsonGenerator.kt:113)
        at com.android.build.gradle.tasks.ExternalNativeBuildJsonTask.doTaskAction(ExternalNativeBuildJsonTask.kt:89)
        at com.android.build.gradle.internal.tasks.UnsafeOutputsTask$taskAction$$inlined$recordTaskAction$1.invoke(BaseTask.kt:66)
        at com.android.build.gradle.internal.tasks.Blocks.recordSpan(Blocks.java:51)
        at com.android.build.gradle.internal.tasks.UnsafeOutputsTask.taskAction(UnsafeOutputsTask.kt:81)
        at jdk.internal.reflect.GeneratedMethodAccessor1070.invoke(Unknown Source)
        at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.base/java.lang.reflect.Method.invoke(Method.java:569)
        at org.gradle.internal.reflect.JavaMethod.invoke(JavaMethod.java:125)
        at org.gradle.api.internal.project.taskfactory.StandardTaskAction.doExecute(StandardTaskAction.java:58)
        at org.gradle.api.internal.project.taskfactory.StandardTaskAction.execute(StandardTaskAction.java:51)
        at org.gradle.api.internal.project.taskfactory.StandardTaskAction.execute(StandardTaskAction.java:29)
        at org.gradle.api.internal.tasks.execution.TaskExecution$3.run(TaskExecution.java:244)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$1.execute(DefaultBuildOperationRunner.java:29)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$1.execute(DefaultBuildOperationRunner.java:26)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:66)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:59)
        at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:166)
        at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:59)
        at org.gradle.internal.operations.DefaultBuildOperationRunner.run(DefaultBuildOperationRunner.java:47)
        at org.gradle.api.internal.tasks.execution.TaskExecution.executeAction(TaskExecution.java:229)
        at org.gradle.api.internal.tasks.execution.TaskExecution.executeActions(TaskExecution.java:212)
        at org.gradle.api.internal.tasks.execution.TaskExecution.executeWithPreviousOutputFiles(TaskExecution.java:195)
        at org.gradle.api.internal.tasks.execution.TaskExecution.execute(TaskExecution.java:162)
        at org.gradle.internal.execution.steps.ExecuteStep.executeInternal(ExecuteStep.java:105)
        at org.gradle.internal.execution.steps.ExecuteStep.access$000(ExecuteStep.java:44)
        at org.gradle.internal.execution.steps.ExecuteStep$1.call(ExecuteStep.java:59)
        at org.gradle.internal.execution.steps.ExecuteStep$1.call(ExecuteStep.java:56)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:209)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:204)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:66)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:59)
        at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:166)
        at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:59)
        at org.gradle.internal.operations.DefaultBuildOperationRunner.call(DefaultBuildOperationRunner.java:53)
        at org.gradle.internal.execution.steps.ExecuteStep.execute(ExecuteStep.java:56)
        at org.gradle.internal.execution.steps.ExecuteStep.execute(ExecuteStep.java:44)
        at org.gradle.internal.execution.steps.CancelExecutionStep.execute(CancelExecutionStep.java:42)
        at org.gradle.internal.execution.steps.TimeoutStep.executeWithoutTimeout(TimeoutStep.java:75)
        at org.gradle.internal.execution.steps.TimeoutStep.execute(TimeoutStep.java:55)
        at org.gradle.internal.execution.steps.PreCreateOutputParentsStep.execute(PreCreateOutputParentsStep.java:50)
        at org.gradle.internal.execution.steps.PreCreateOutputParentsStep.execute(PreCreateOutputParentsStep.java:28)
        at org.gradle.internal.execution.steps.RemovePreviousOutputsStep.execute(RemovePreviousOutputsStep.java:67)
        at org.gradle.internal.execution.steps.RemovePreviousOutputsStep.execute(RemovePreviousOutputsStep.java:37)
        at org.gradle.internal.execution.steps.BroadcastChangingOutputsStep.execute(BroadcastChangingOutputsStep.java:61)
        at org.gradle.internal.execution.steps.BroadcastChangingOutputsStep.execute(BroadcastChangingOutputsStep.java:26)
        at org.gradle.internal.execution.steps.CaptureOutputsAfterExecutionStep.execute(CaptureOutputsAfterExecutionStep.java:69)
        at org.gradle.internal.execution.steps.CaptureOutputsAfterExecutionStep.execute(CaptureOutputsAfterExecutionStep.java:46)
        at org.gradle.internal.execution.steps.ResolveInputChangesStep.execute(ResolveInputChangesStep.java:40)
        at org.gradle.internal.execution.steps.ResolveInputChangesStep.execute(ResolveInputChangesStep.java:29)
        at org.gradle.internal.execution.steps.BuildCacheStep.executeWithoutCache(BuildCacheStep.java:189)
        at org.gradle.internal.execution.steps.BuildCacheStep.lambda$execute$1(BuildCacheStep.java:75)
        at org.gradle.internal.Either$Right.fold(Either.java:175)
        at org.gradle.internal.execution.caching.CachingState.fold(CachingState.java:62)
        at org.gradle.internal.execution.steps.BuildCacheStep.execute(BuildCacheStep.java:73)
        at org.gradle.internal.execution.steps.BuildCacheStep.execute(BuildCacheStep.java:48)
        at org.gradle.internal.execution.steps.StoreExecutionStateStep.execute(StoreExecutionStateStep.java:46)
        at org.gradle.internal.execution.steps.StoreExecutionStateStep.execute(StoreExecutionStateStep.java:35)
        at org.gradle.internal.execution.steps.SkipUpToDateStep.executeBecause(SkipUpToDateStep.java:75)
        at org.gradle.internal.execution.steps.SkipUpToDateStep.lambda$execute$2(SkipUpToDateStep.java:53)
        at java.base/java.util.Optional.orElseGet(Optional.java:364)
        at org.gradle.internal.execution.steps.SkipUpToDateStep.execute(SkipUpToDateStep.java:53)
        at org.gradle.internal.execution.steps.SkipUpToDateStep.execute(SkipUpToDateStep.java:35)
        at org.gradle.internal.execution.steps.legacy.MarkSnapshottingInputsFinishedStep.execute(MarkSnapshottingInputsFinishedStep.java:37)
        at org.gradle.internal.execution.steps.legacy.MarkSnapshottingInputsFinishedStep.execute(MarkSnapshottingInputsFinishedStep.java:27)
        at org.gradle.internal.execution.steps.ResolveIncrementalCachingStateStep.executeDelegate(ResolveIncrementalCachingStateStep.java:49)
        at org.gradle.internal.execution.steps.ResolveIncrementalCachingStateStep.executeDelegate(ResolveIncrementalCachingStateStep.java:27)
        at org.gradle.internal.execution.steps.AbstractResolveCachingStateStep.execute(AbstractResolveCachingStateStep.java:71)
        at org.gradle.internal.execution.steps.AbstractResolveCachingStateStep.execute(AbstractResolveCachingStateStep.java:39)
        at org.gradle.internal.execution.steps.ResolveChangesStep.execute(ResolveChangesStep.java:65)
        at org.gradle.internal.execution.steps.ResolveChangesStep.execute(ResolveChangesStep.java:36)
        at org.gradle.internal.execution.steps.ValidateStep.execute(ValidateStep.java:107)
        at org.gradle.internal.execution.steps.ValidateStep.execute(ValidateStep.java:56)
        at org.gradle.internal.execution.steps.AbstractCaptureStateBeforeExecutionStep.execute(AbstractCaptureStateBeforeExecutionStep.java:64)
        at org.gradle.internal.execution.steps.AbstractCaptureStateBeforeExecutionStep.execute(AbstractCaptureStateBeforeExecutionStep.java:43)
        at org.gradle.internal.execution.steps.AbstractSkipEmptyWorkStep.executeWithNonEmptySources(AbstractSkipEmptyWorkStep.java:125)
        at org.gradle.internal.execution.steps.AbstractSkipEmptyWorkStep.execute(AbstractSkipEmptyWorkStep.java:56)
        at org.gradle.internal.execution.steps.AbstractSkipEmptyWorkStep.execute(AbstractSkipEmptyWorkStep.java:36)
        at org.gradle.internal.execution.steps.legacy.MarkSnapshottingInputsStartedStep.execute(MarkSnapshottingInputsStartedStep.java:38)
        at org.gradle.internal.execution.steps.LoadPreviousExecutionStateStep.execute(LoadPreviousExecutionStateStep.java:36)
        at org.gradle.internal.execution.steps.LoadPreviousExecutionStateStep.execute(LoadPreviousExecutionStateStep.java:23)
        at org.gradle.internal.execution.steps.HandleStaleOutputsStep.execute(HandleStaleOutputsStep.java:75)
        at org.gradle.internal.execution.steps.HandleStaleOutputsStep.execute(HandleStaleOutputsStep.java:41)
        at org.gradle.internal.execution.steps.AssignMutableWorkspaceStep.lambda$execute$0(AssignMutableWorkspaceStep.java:35)
        at org.gradle.api.internal.tasks.execution.TaskExecution$4.withWorkspace(TaskExecution.java:289)
        at org.gradle.internal.execution.steps.AssignMutableWorkspaceStep.execute(AssignMutableWorkspaceStep.java:31)
        at org.gradle.internal.execution.steps.AssignMutableWorkspaceStep.execute(AssignMutableWorkspaceStep.java:22)
        at org.gradle.internal.execution.steps.ChoosePipelineStep.execute(ChoosePipelineStep.java:40)
        at org.gradle.internal.execution.steps.ChoosePipelineStep.execute(ChoosePipelineStep.java:23)
        at org.gradle.internal.execution.steps.ExecuteWorkBuildOperationFiringStep.lambda$execute$2(ExecuteWorkBuildOperationFiringStep.java:67)
        at java.base/java.util.Optional.orElseGet(Optional.java:364)
        at org.gradle.internal.execution.steps.ExecuteWorkBuildOperationFiringStep.execute(ExecuteWorkBuildOperationFiringStep.java:67)
        at org.gradle.internal.execution.steps.ExecuteWorkBuildOperationFiringStep.execute(ExecuteWorkBuildOperationFiringStep.java:39)
        at org.gradle.internal.execution.steps.IdentityCacheStep.execute(IdentityCacheStep.java:46)
        at org.gradle.internal.execution.steps.IdentityCacheStep.execute(IdentityCacheStep.java:34)
        at org.gradle.internal.execution.steps.IdentifyStep.execute(IdentifyStep.java:48)
        at org.gradle.internal.execution.steps.IdentifyStep.execute(IdentifyStep.java:35)
        at org.gradle.internal.execution.impl.DefaultExecutionEngine$1.execute(DefaultExecutionEngine.java:61)
        at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.executeIfValid(ExecuteActionsTaskExecuter.java:127)
        at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.execute(ExecuteActionsTaskExecuter.java:116)
        at org.gradle.api.internal.tasks.execution.FinalizePropertiesTaskExecuter.execute(FinalizePropertiesTaskExecuter.java:46)
        at org.gradle.api.internal.tasks.execution.ResolveTaskExecutionModeExecuter.execute(ResolveTaskExecutionModeExecuter.java:51)
        at org.gradle.api.internal.tasks.execution.SkipTaskWithNoActionsExecuter.execute(SkipTaskWithNoActionsExecuter.java:57)
        at org.gradle.api.internal.tasks.execution.SkipOnlyIfTaskExecuter.execute(SkipOnlyIfTaskExecuter.java:74)
        at org.gradle.api.internal.tasks.execution.CatchExceptionTaskExecuter.execute(CatchExceptionTaskExecuter.java:36)
        at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.executeTask(EventFiringTaskExecuter.java:77)
        at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.call(EventFiringTaskExecuter.java:55)
        at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.call(EventFiringTaskExecuter.java:52)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:209)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:204)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:66)
        at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:59)
        at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:166)
        at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:59)
        at org.gradle.internal.operations.DefaultBuildOperationRunner.call(DefaultBuildOperationRunner.java:53)
        at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter.execute(EventFiringTaskExecuter.java:52)
        at org.gradle.execution.plan.LocalTaskNodeExecutor.execute(LocalTaskNodeExecutor.java:42)
        at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$InvokeNodeExecutorsAction.execute(DefaultTaskExecutionGraph.java:331)
        at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$InvokeNodeExecutorsAction.execute(DefaultTaskExecutionGraph.java:318)
        at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$BuildOperationAwareExecutionAction.lambda$execute$0(DefaultTaskExecutionGraph.java:314)   
        at org.gradle.internal.operations.CurrentBuildOperationRef.with(CurrentBuildOperationRef.java:85)
        at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$BuildOperationAwareExecutionAction.execute(DefaultTaskExecutionGraph.java:314)
        at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$BuildOperationAwareExecutionAction.execute(DefaultTaskExecutionGraph.java:303)
        at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker.execute(DefaultPlanExecutor.java:459)
        at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker.run(DefaultPlanExecutor.java:376)
        at org.gradle.internal.concurrent.ExecutorPolicy$CatchAndRecordFailures.onExecute(ExecutorPolicy.java:64)
        at org.gradle.internal.concurrent.AbstractManagedExecutor$1.run(AbstractManagedExecutor.java:48)
        at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1136)
        at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:635)
        at java.base/java.lang.Thread.run(Thread.java:840)
  Caused by: com.android.ide.common.process.ProcessException: Error while executing process C:\Users\vj2k0\AppData\Local\Android\Sdk\cmake\3.22.1\bin\cmake.exe with arguments {-HE:\Development\apeers-app\node_modules\react-native\ReactAndroid\cmake-utils\default-app-setup -DCMAKE_SYSTEM_NAME=Android -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DCMAKE_SYSTEM_VERSION=24 -DANDROID_PLATFORM=android-24 -DANDROID_ABI=arm64-v8a -DCMAKE_ANDROID_ARCH_ABI=arm64-v8a -DANDROID_NDK=C:\Users\vj2k0\AppData\Local\Android\Sdk\ndk\26.1.10909125 -DCMAKE_ANDROID_NDK=C:\Users\vj2k0\AppData\Local\Android\Sdk\ndk\26.1.10909125 -DCMAKE_TOOLCHAIN_FILE=C:\Users\vj2k0\AppData\Local\Android\Sdk\ndk\26.1.10909125\build\cmake\android.toolchain.cmake -DCMAKE_MAKE_PROGRAM=C:\Users\vj2k0\AppData\Local\Android\Sdk\cmake\3.22.1\bin\ninja.exe -DCMAKE_LIBRARY_OUTPUT_DIRECTORY=E:\Development\apeers-app\android\app\build\intermediates\cxx\Debug\z2z38611\obj\arm64-v8a -DCMAKE_RUNTIME_OUTPUT_DIRECTORY=E:\Development\apeers-app\android\app\build\intermediates\cxx\Debug\z2z38611\obj\arm64-v8a -DCMAKE_BUILD_TYPE=Debug -DCMAKE_FIND_ROOT_PATH=E:\Development\apeers-app\android\app\.cxx\Debug\z2z38611\prefab\arm64-v8a\prefab -BE:\Development\apeers-app\android\app\.cxx\Debug\z2z38611\arm64-v8a -GNinja -DPROJECT_BUILD_DIR=E:\Development\apeers-app\android\app\build -DREACT_ANDROID_DIR=E:\Development\apeers-app\node_modules\react-native\ReactAndroid -DANDROID_STL=c++_shared -DANDROID_USE_LEGACY_TOOLCHAIN_FILE=ON}
        at com.android.build.gradle.internal.process.GradleProcessResult.buildProcessException(GradleProcessResult.java:73)
        at com.android.build.gradle.internal.process.GradleProcessResult.assertNormalExitValue(GradleProcessResult.java:48)
        at com.android.build.gradle.internal.cxx.process.ExecuteProcessKt.execute(ExecuteProcess.kt:277)
        ... 140 more
  Caused by: org.gradle.process.internal.ExecException: Process 'command 'C:\Users\vj2k0\AppData\Local\Android\Sdk\cmake\3.22.1\bin\cmake.exe'' finished with non-zero exit value 1
        at org.gradle.process.internal.DefaultExecHandle$ExecResultImpl.assertNormalExitValue(DefaultExecHandle.java:442)
        at com.android.build.gradle.internal.process.GradleProcessResult.assertNormalExitValue(GradleProcessResult.java:46)
        ... 141 more


* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.
> Get more help at https://help.gradle.org.

BUILD FAILED in 10s
419 actionable tasks: 24 executed, 395 up-to-date
Error: E:\Development\apeers-app\android\gradlew.bat app:assembleDebug -x lint -x test --configure-on-demand --build-cache -PreactNativeDevServerPort=8081 -PreactNativeArchitectures=arm64-v8a,armeabi-v7a exited with non-zero code: 1
Error: E:\Development\apeers-app\android\gradlew.bat app:assembleDebug -x lint -x test --configure-on-demand --build-cache -PreactNativeDevServerPort=8081 -PreactNativeArchitectures=arm64-v8a,armeabi-v7a exited with non-zero code: 1
    at ChildProcess.completionListener (E:\Development\apeers-app\node_modules\@expo\spawn-async\src\spawnAsync.ts:67:13)
    at Object.onceWrapper (node:events:634:26)
    at ChildProcess.emit (node:events:519:28)
    at ChildProcess.cp.emit (E:\Development\apeers-app\node_modules\cross-spawn\lib\enoent.js:34:29)
    at maybeClose (node:internal/child_process:1105:16)
    at Process.ChildProcess._handle.onexit (node:internal/child_process:305:5)
    ...
    at spawnAsync (E:\Development\apeers-app\node_modules\@expo\spawn-async\src\spawnAsync.ts:28:21)
    at spawnGradleAsync (E:\Development\apeers-app\node_modules\@expo\cli\src\start\platforms\android\gradle.ts:134:28)
    at assembleAsync (E:\Development\apeers-app\node_modules\@expo\cli\src\start\platforms\android\gradle.ts:83:16)
    at runAndroidAsync (E:\Development\apeers-app\node_modules\@expo\cli\src\run\android\runAndroidAsync.ts:48:24)
error: script "android" exited with code 1
