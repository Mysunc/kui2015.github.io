---
layout: post
title: Android֮�ã����� -- �Ĵ����֮Service
category: Android
tags: [Android]
excerpt: >
  ˵����Activity���������ڣ�������˵˵Service��

service����Activity�����Ƶ���������Ƕ���Ҫ�̳и��࣬����Ҫ��AndroidManifest.xml�����ã��������serviceû
---

˵����Activity���������ڣ�������˵˵Service��

Service����Activity�����Ƶ���������Ƕ���Ҫ�̳и��࣬����Ҫ��AndroidManifest.xml�����ã��������serviceû�н��档�����ȼ��ϣ�Service�Ȳ���Ծ��Activity�ߡ�

####����˵˵Service���������ڣ�Service���������������Activity��˵��һ�㣬��ͼ

![Alt text](./1415768381287.png)

����Ƿǰ󶨵�: onCreate() --> onStartCommand() --> onDestory();
    onStartCommand()�������滻onStart()�����ģ��ȸ轨�������·���onStartCommand(),�������ȥ�鿴Դ�룬�ᷢ����ʵonStartCommand()�����ǽ��ϵ�: ����onStartCommand()����ֵ�������������˵��
``` java
public int onStartCommand(Intent intent, int flags, int startId) {
    onStart(intent, startId);
    return mStartCompatibility ? START_STICKY_COMPATIBILITY : START_STICKY;
}
```
���������ұߵ�ͼ��
�ұ��ǰ󶨵�: onCreate() --> onBind() --> onUnbind() --> onDestory();

��Service�����������У�onCreate()����ֻ�ᱻ����һ�Ρ���onStartCommand()�������Ա����ö�Σ�onBind()�ȷ���Ҳֻ�ܵ���һ�Σ�����˵������onStartCommand()�����⣬����������һ������������ֻ�ܱ�����һ�Ρ�

####������˵˵������߻쵽һ������
��ʱֻҪ��ס��bind��ʱ����stop;
���������startService()����ֻ����bindΪ��ʱ��stopServivce()������Service;

####IntendService

Service������UI�߳��У����ܷ������磬Ҳ���ܽ��к�ʱ�Ĳ�������������ANR�����Գ�����IntenService��
IntentService��һ�������첽������࣬����Service�����࣬���ǿ���ͬ��ʹ��startService(intent)����������Ȼ����дIntentService�е�onHandleIntent()������ִ��һЩ��ʱ������
��Ҫע����ǣ�IntentService������ͬ����onStartCommand()��������Ҳ������дonStartCommand()������������ͨService����һ���ġ���IntentService�У�onStartCommand()��������onHandleIntent()����ִ�С�onHandleIntent()����������ִ�н������Զ����١�

####����̵���Service




####Service���ȼ�













