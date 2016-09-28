# TestAndroid
如果Tasks 设置为clean assembleRelease
报
Task 'clean' not found in root project 'workspace'.或
Task 'assembleRelease' not found in root project 'workspace'.
错误，是因为
/Users/user/.jenkins/jobs/TestAndroid/workspace/TestAndroid
路径下没有build.gradle
这个build.gradle被放在/Users/user/.jenkins/jobs/TestAndroid/workspace/TestAndroid/build.gradle
将jenkins下TestAndroid配置里边的Build File项填上${WORKSPACE}/TestAndroid/build.gradle
可以解决问题
