---
title: "[Jenkins] 젠킨스(Jenkins) 에러"
layout: single
categories: Jenkins
tag: [Jenkins]
toc: true
toc_sticky: true
toc_icon: "bars"
toc_label: "Table of Contents"
---

## 에러
- 해결방법1 : `skip-certificate-check` 플러그인 수동 다운로드

```
sun.security.provider.certpath.SunCertPathBuilderException: unable to find valid certification path to requested target
	at java.base/sun.security.provider.certpath.SunCertPathBuilder.build(SunCertPathBuilder.java:141)
	at java.base/sun.security.provider.certpath.SunCertPathBuilder.engineBuild(SunCertPathBuilder.java:126)
	at java.base/java.security.cert.CertPathBuilder.build(CertPathBuilder.java:297)
	at java.base/sun.security.validator.PKIXValidator.doBuild(PKIXValidator.java:380)
Caused: sun.security.validator.ValidatorException: PKIX path building failed
	at java.base/sun.security.validator.PKIXValidator.doBuild(PKIXValidator.java:385)
	at java.base/sun.security.validator.PKIXValidator.engineValidate(PKIXValidator.java:290)
	at java.base/sun.security.validator.Validator.validate(Validator.java:264)
	at java.base/sun.security.ssl.X509TrustManagerImpl.validate(X509TrustManagerImpl.java:321)
	at java.base/sun.security.ssl.X509TrustManagerImpl.checkTrusted(X509TrustManagerImpl.java:221)
	at java.base/sun.security.ssl.X509TrustManagerImpl.checkServerTrusted(X509TrustManagerImpl.java:129)
	at java.base/sun.security.ssl.CertificateMessage$T13CertificateConsumer.checkServerCerts(CertificateMessage.java:1313)
Caused: javax.net.ssl.SSLHandshakeException: PKIX path building failed: sun.security.provider.certpath.SunCertPathBuilderException: unable to find valid certification path to requested target
	at java.base/sun.security.ssl.Alert.createSSLException(Alert.java:128)
	at java.base/sun.security.ssl.TransportContext.fatal(TransportContext.java:321)
	at java.base/sun.security.ssl.TransportContext.fatal(TransportContext.java:264)
	at java.base/sun.security.ssl.TransportContext.fatal(TransportContext.java:259)
	at java.base/sun.security.ssl.CertificateMessage$T13CertificateConsumer.checkServerCerts(CertificateMessage.java:1329)
	at java.base/sun.security.ssl.CertificateMessage$T13CertificateConsumer.onConsumeCertificate(CertificateMessage.java:1204)
	at java.base/sun.security.ssl.CertificateMessage$T13CertificateConsumer.consume(CertificateMessage.java:1151)
	at java.base/sun.security.ssl.SSLHandshake.consume(SSLHandshake.java:392)
	at java.base/sun.security.ssl.HandshakeContext.dispatch(HandshakeContext.java:444)
	at java.base/sun.security.ssl.HandshakeContext.dispatch(HandshakeContext.java:421)
	at java.base/sun.security.ssl.TransportContext.dispatch(TransportContext.java:178)
	at java.base/sun.security.ssl.SSLTransport.decode(SSLTransport.java:164)
	at java.base/sun.security.ssl.SSLSocketImpl.decode(SSLSocketImpl.java:1152)
	at java.base/sun.security.ssl.SSLSocketImpl.readHandshakeRecord(SSLSocketImpl.java:1063)
	at java.base/sun.security.ssl.SSLSocketImpl.startHandshake(SSLSocketImpl.java:402)
	at java.base/sun.net.www.protocol.https.HttpsClient.afterConnect(HttpsClient.java:567)
	at java.base/sun.net.www.protocol.https.AbstractDelegateHttpsURLConnection.connect(AbstractDelegateHttpsURLConnection.java:185)
	at java.base/sun.net.www.protocol.http.HttpURLConnection.followRedirect0(HttpURLConnection.java:2758)
	at java.base/sun.net.www.protocol.http.HttpURLConnection.followRedirect(HttpURLConnection.java:2680)
	at java.base/sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1843)
	at java.base/sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1509)
	at java.base/sun.net.www.protocol.https.HttpsURLConnectionImpl.getInputStream(HttpsURLConnectionImpl.java:245)
	at hudson.model.UpdateCenter$UpdateCenterConfiguration.download(UpdateCenter.java:1291)
Caused: java.io.IOException: Failed to load https://updates.jenkins.io/download/plugins/sshd/3.242.va_db_9da_b_26a_c3/sshd.hpi to C:\ProgramData\Jenkins\.jenkins\plugins\sshd.jpi.tmp
	at hudson.model.UpdateCenter$UpdateCenterConfiguration.download(UpdateCenter.java:1302)
Caused: java.io.IOException: Failed to download from https://updates.jenkins.io/download/plugins/sshd/3.242.va_db_9da_b_26a_c3/sshd.hpi (redirected to: https://get.jenkins.io/plugins/sshd/3.242.va_db_9da_b_26a_c3/sshd.hpi)
	at hudson.model.UpdateCenter$UpdateCenterConfiguration.download(UpdateCenter.java:1336)
	at hudson.model.UpdateCenter$DownloadJob._run(UpdateCenter.java:1893)
	at hudson.model.UpdateCenter$InstallationJob._run(UpdateCenter.java:2205)
	at hudson.model.UpdateCenter$DownloadJob.run(UpdateCenter.java:1867)
	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:515)
	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
	at hudson.remoting.AtmostOneThreadExecutor$Worker.run(AtmostOneThreadExecutor.java:121)
	at java.base/java.lang.Thread.run(Thread.java:834)
```