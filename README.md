# Error-log
appointment openmrs error log

24-07-2017 05:22:52 [WARN ] RefillIdentifierPoolsTask - Not running scheduled task. DaemonToken = null; enabled = false
24-07-2017 05:22:54 [WARN ] SimpleUrlHandlerMapping - Neither 'urlMap' nor 'mappings' set on SimpleUrlHandlerMapping
24-07-2017 05:23:01 [ERROR] OpenElisPatientFailedEventsFeedClientImpl - openelisatomfeedclient:failed feed execution while running failed eventsjava.lang.NullPointerException
java.lang.NullPointerException
        at org.bahmni.module.bahmnicore.properties.BahmniCoreProperties.getProperty(BahmniCoreProperties.java:28)
        at org.bahmni.module.elisatomfeedclient.api.ElisAtomFeedProperties.getPatientFeedUri(ElisAtomFeedProperties.java:19)
        at org.bahmni.module.elisatomfeedclient.api.client.impl.OpenElisPatientFailedEventsFeedClientImpl.getFeedUri(OpenElisPatientFailedEventsFeedClientImpl.java:44)
        at org.bahmni.module.elisatomfeedclient.api.client.OpenElisFeedClient.createAtomFeedClient(OpenElisFeedClient.java:55)
        at org.bahmni.module.elisatomfeedclient.api.client.OpenElisFeedClient.getAtomFeedClient(OpenElisFeedClient.java:49)
        at org.bahmni.module.elisatomfeedclient.api.client.impl.OpenElisPatientFailedEventsFeedClientImpl.processFailedEvents(OpenElisPatientFailedEventsFeedClientImpl.java:64)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(Unknown Source)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(Unknown Source)
        at java.lang.reflect.Method.invoke(Unknown Source)
        at org.springframework.aop.support.AopUtils.invokeJoinpointUsingReflection(AopUtils.java:317)
        at org.springframework.aop.framework.JdkDynamicAopProxy.invoke(JdkDynamicAopProxy.java:201)
        at com.sun.proxy.$Proxy304.processFailedEvents(Unknown Source)
        at org.bahmni.module.elisatomfeedclient.api.task.OpenElisPatientFeedFailedEventsTask.execute(OpenElisPatientFeedFailedEventsTask.java:13)
        at org.openmrs.scheduler.tasks.TaskThreadedInitializationWrapper.execute(TaskThreadedInitializationWrapper.java:67)
        at org.openmrs.scheduler.timer.TimerSchedulerTask.execute(TimerSchedulerTask.java:94)
        at org.openmrs.api.context.Daemon$2.run(Daemon.java:135)
24-07-2017 05:23:01 [ERROR] TimerSchedulerTask - FATAL ERROR: Task [class org.openmrs.scheduler.tasks.TaskThreadedInitializationWrapper] failed due to exception [java.lang.RuntimeException]
java.lang.RuntimeException: java.lang.NullPointerException
        at org.bahmni.module.elisatomfeedclient.api.client.impl.OpenElisPatientFailedEventsFeedClientImpl.processFailedEvents(OpenElisPatientFailedEventsFeedClientImpl.java:75)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(Unknown Source)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(Unknown Source)
        at java.lang.reflect.Method.invoke(Unknown Source)
        at org.springframework.aop.support.AopUtils.invokeJoinpointUsingReflection(AopUtils.java:317)
        at org.springframework.aop.framework.JdkDynamicAopProxy.invoke(JdkDynamicAopProxy.java:201)
        at com.sun.proxy.$Proxy304.processFailedEvents(Unknown Source)
        at org.bahmni.module.elisatomfeedclient.api.task.OpenElisPatientFeedFailedEventsTask.execute(OpenElisPatientFeedFailedEventsTask.java:13)
        at org.openmrs.scheduler.tasks.TaskThreadedInitializationWrapper.execute(TaskThreadedInitializationWrapper.java:67)
        at org.openmrs.scheduler.timer.TimerSchedulerTask.execute(TimerSchedulerTask.java:94)
        at org.openmrs.api.context.Daemon$2.run(Daemon.java:135)
Caused by: java.lang.NullPointerException
        at org.bahmni.module.bahmnicore.properties.BahmniCoreProperties.getProperty(BahmniCoreProperties.java:28)
        at org.bahmni.module.elisatomfeedclient.api.ElisAtomFeedProperties.getPatientFeedUri(ElisAtomFeedProperties.java:19)
        at org.bahmni.module.elisatomfeedclient.api.client.impl.OpenElisPatientFailedEventsFeedClientImpl.getFeedUri(OpenElisPatientFailedEventsFeedClientImpl.java:44)
        at org.bahmni.module.elisatomfeedclient.api.client.OpenElisFeedClient.createAtomFeedClient(OpenElisFeedClient.java:55)
        at org.bahmni.module.elisatomfeedclient.api.client.OpenElisFeedClient.getAtomFeedClient(OpenElisFeedClient.java:49)
        at org.bahmni.module.elisatomfeedclient.api.client.impl.OpenElisPatientFailedEventsFeedClientImpl.processFailedEvents(OpenElisPatientFailedEventsFeedClientImpl.java:64)
        ... 11 more
24-07-2017 05:23:05 [ERROR] SqlExceptionHelper - Cannot delete or update a parent row: a foreign key constraint fails (`openmrs`.`concept`, CONSTRAINT `concept_classes` FOREIGN KEY (`class_id`) REFERENCES `concept_class` (`concept_class_id`))
24-07-2017 05:23:05 [ERROR] BatchingBatch - HHH000315: Exception executing batch [could not execute batch]
24-07-2017 05:23:05 [WARN ] ModuleUtil - Unable to invoke started() method on the module's activator
org.springframework.dao.DataIntegrityViolationException: could not execute batch; SQL [delete from concept_class where concept_class_id=?]; constraint [null]; nested exception is org.hibernate.exception.ConstraintViolationException: could not execute batch
        at org.springframework.orm.hibernate4.SessionFactoryUtils.convertHibernateAccessException(SessionFactoryUtils.java:163)
        at org.springframework.orm.hibernate4.HibernateTransactionManager.convertHibernateAccessException(HibernateTransactionManager.java:730)
        at org.springframework.orm.hibernate4.HibernateTransactionManager.doCommit(HibernateTransactionManager.java:592)
        at org.springframework.transaction.support.AbstractPlatformTransactionManager.processCommit(AbstractPlatformTransactionManager.java:757)
        at org.springframework.transaction.support.AbstractPlatformTransactionManager.commit(AbstractPlatformTransactionManager.java:726)
        at org.springframework.transaction.interceptor.TransactionAspectSupport.commitTransactionAfterReturning(TransactionAspectSupport.java:515)
        at org.springframework.transaction.interceptor.TransactionAspectSupport.invokeWithinTransaction(TransactionAspectSupport.java:291)
        at org.springframework.transaction.interceptor.TransactionInterceptor.invoke(TransactionInterceptor.java:96)
        at org.springframework.aop.framework.ReflectiveMethodInvocation.proceed(ReflectiveMethodInvocation.java:179)
        at org.springframework.aop.framework.JdkDynamicAopProxy.invoke(JdkDynamicAopProxy.java:207)
        at com.sun.proxy.$Proxy155.purgeConceptClass(Unknown Source)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(Unknown Source)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(Unknown Source)
        at java.lang.reflect.Method.invoke(Unknown Source)
        at org.springframework.aop.support.AopUtils.invokeJoinpointUsingReflection(AopUtils.java:317)
        at org.springframework.aop.framework.ReflectiveMethodInvocation.invokeJoinpoint(ReflectiveMethodInvocation.java:190)
        at org.springframework.aop.framework.ReflectiveMethodInvocation.proceed(ReflectiveMethodInvocation.java:157)
        at org.springframework.aop.framework.adapter.AfterReturningAdviceInterceptor.invoke(AfterReturningAdviceInterceptor.java:52)
        at org.springframework.aop.framework.ReflectiveMethodInvocation.proceed(ReflectiveMethodInvocation.java:179)
        at org.springframework.cache.interceptor.CacheInterceptor$1.invoke(CacheInterceptor.java:52)
        at org.springframework.cache.interceptor.CacheAspectSupport.execute(CacheAspectSupport.java:303)
        at org.springframework.cache.interceptor.CacheInterceptor.invoke(CacheInterceptor.java:61)
        at org.springframework.aop.framework.ReflectiveMethodInvocation.proceed(ReflectiveMethodInvocation.java:179)
        at org.openmrs.aop.LoggingAdvice.invoke(LoggingAdvice.java:121)
        at org.springframework.aop.framework.ReflectiveMethodInvocation.proceed(ReflectiveMethodInvocation.java:179)
        at org.springframework.aop.framework.adapter.MethodBeforeAdviceInterceptor.invoke(MethodBeforeAdviceInterceptor.java:52)
        at org.springframework.aop.framework.ReflectiveMethodInvocation.proceed(ReflectiveMethodInvocation.java:179)
        at org.springframework.aop.framework.adapter.MethodBeforeAdviceInterceptor.invoke(MethodBeforeAdviceInterceptor.java:52)
        at org.springframework.aop.framework.ReflectiveMethodInvocation.proceed(ReflectiveMethodInvocation.java:179)
        at org.springframework.aop.framework.JdkDynamicAopProxy.invoke(JdkDynamicAopProxy.java:207)
        at com.sun.proxy.$Proxy156.purgeConceptClass(Unknown Source)
        at org.openmrs.module.referencemetadata.ReferenceMetadataActivator.installConcepts(ReferenceMetadataActivator.java:89)
        at org.openmrs.module.referencemetadata.ReferenceMetadataActivator.started(ReferenceMetadataActivator.java:61)
        at org.openmrs.module.ModuleUtil.refreshApplicationContext(ModuleUtil.java:933)
        at org.openmrs.module.web.WebModuleUtil.refreshWAC(WebModuleUtil.java:866)
        at org.openmrs.web.Listener.performWebStartOfModules(Listener.java:656)
        at org.openmrs.web.Listener.performWebStartOfModules(Listener.java:635)
        at org.openmrs.web.Listener.startOpenmrs(Listener.java:266)
        at org.openmrs.web.WebDaemon$1.run(WebDaemon.java:42)
Caused by: org.hibernate.exception.ConstraintViolationException: could not execute batch
        at org.hibernate.exception.internal.SQLStateConversionDelegate.convert(SQLStateConversionDelegate.java:129)
        at org.hibernate.exception.internal.StandardSQLExceptionConverter.convert(StandardSQLExceptionConverter.java:49)
        at org.hibernate.engine.jdbc.spi.SqlExceptionHelper.convert(SqlExceptionHelper.java:126)
        at org.hibernate.engine.jdbc.batch.internal.BatchingBatch.performExecution(BatchingBatch.java:136)
        at org.hibernate.engine.jdbc.batch.internal.BatchingBatch.doExecuteBatch(BatchingBatch.java:114)
        at org.hibernate.engine.jdbc.batch.internal.AbstractBatchImpl.execute(AbstractBatchImpl.java:163)
        at org.hibernate.engine.jdbc.internal.JdbcCoordinatorImpl.executeBatch(JdbcCoordinatorImpl.java:226)
        at org.hibernate.engine.spi.ActionQueue.executeActions(ActionQueue.java:484)
        at org.hibernate.engine.spi.ActionQueue.executeActions(ActionQueue.java:351)
        at org.hibernate.event.internal.AbstractFlushingEventListener.performExecutions(AbstractFlushingEventListener.java:350)
        at org.hibernate.event.internal.DefaultFlushEventListener.onFlush(DefaultFlushEventListener.java:56)
        at org.hibernate.internal.SessionImpl.flush(SessionImpl.java:1258)
        at org.hibernate.internal.SessionImpl.managedFlush(SessionImpl.java:425)
        at org.hibernate.engine.transaction.internal.jdbc.JdbcTransaction.beforeTransactionCommit(JdbcTransaction.java:101)
        at org.hibernate.engine.transaction.spi.AbstractTransactionImpl.commit(AbstractTransactionImpl.java:177)
        at org.springframework.orm.hibernate4.HibernateTransactionManager.doCommit(HibernateTransactionManager.java:584)
        ... 37 more
Caused by: java.sql.BatchUpdateException: Cannot delete or update a parent row: a foreign key constraint fails (`openmrs`.`concept`, CONSTRAINT `concept_classes` FOREIGN KEY (`class_id`) REFERENCES `concept_class` (`concept_class_id`))
        at com.mysql.jdbc.PreparedStatement.executeBatchSerially(PreparedStatement.java:2055)
        at com.mysql.jdbc.PreparedStatement.executeBatch(PreparedStatement.java:1467)
        at com.mchange.v2.c3p0.impl.NewProxyPreparedStatement.executeBatch(NewProxyPreparedStatement.java:1135)
        at org.hibernate.engine.jdbc.batch.internal.BatchingBatch.performExecution(BatchingBatch.java:127)
        ... 49 more
Caused by: com.mysql.jdbc.exceptions.jdbc4.MySQLIntegrityConstraintViolationException: Cannot delete or update a parent row: a foreign key constraint fails (`openmrs`.`concept`, CONSTRAINT `concept_classes` FOREIGN KEY (`class_id`) REFERENCES `concept_class` (`concept_class_id`))
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(Unknown Source)
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(Unknown Source)
        at java.lang.reflect.Constructor.newInstance(Unknown Source)
        at com.mysql.jdbc.Util.handleNewInstance(Util.java:411)
        at com.mysql.jdbc.Util.getInstance(Util.java:386)
        at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:1041)
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:4237)
        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:4169)
        at com.mysql.jdbc.MysqlIO.sendCommand(MysqlIO.java:2617)
        at com.mysql.jdbc.MysqlIO.sqlQueryDirect(MysqlIO.java:2778)
        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2825)
        at com.mysql.jdbc.PreparedStatement.executeInternal(PreparedStatement.java:2156)
        at com.mysql.jdbc.PreparedStatement.executeUpdate(PreparedStatement.java:2441)
        at com.mysql.jdbc.PreparedStatement.executeBatchSerially(PreparedStatement.java:2007)
        ... 52 more
24-07-2017 05:23:06 [ERROR] LogErrorHandler - Line=356 The content of element type "dwr" must match "(init?,allow?,signatures?)".
24-07-2017 05:23:06 [ERROR] SignatureParser - Parameter mismatch parsing signatures section in dwr.xml on line: DWRHtmlFormEntryService.checkIfLoggedIn()
24-07-2017 05:23:06 [WARN ] OpenmrsUtil - Unable to find a runtime properties file at /openmrs-runtime.properties
Jul 24, 2017 5:23:10 AM org.apache.catalina.util.SessionIdGeneratorBase createSecureRandom
INFO: Creation of SecureRandom instance for session ID generation using [SHA1PRNG] took [3,219] milliseconds.
24-07-2017 05:23:10 [WARN ] OpenmrsUtil - Unable to find a runtime properties file at /openmrs-runtime.properties
Jul 24, 2017 5:23:10 AM org.apache.coyote.AbstractProtocol start
INFO: Starting ProtocolHandler ["http-nio-8050"]
Jul 24, 2017 5:23:10 AM org.apache.catalina.core.ApplicationContext log
INFO: Initializing Spring FrameworkServlet 'openmrs'
Jul 24, 2017 5:23:59 AM org.apache.catalina.core.ApplicationContext log
INFO: Initializing Spring FrameworkServlet 'openmrs_static_content'

