---
layout: post
title: Android֮�ã����� -- �Ĵ����֮service
category: Android
tags: [Android]
excerpt: >
  ˵����Activity���������ڣ�������˵˵service��

service����Activity�����Ƶ���������Ƕ���Ҫ�̳и��࣬����Ҫ��AndroidManifest.xml�����ã��������serviceû
---

˵����Activity���������ڣ�������˵˵service��

service����Activity�����Ƶ���������Ƕ���Ҫ�̳и��࣬����Ҫ��AndroidManifest.xml�����ã��������serviceû�н��档

####����˵˵service���������ڣ�service���������������Activity��˵��һ�㣬��ͼ

![Alt text](./1415768381287.png)

����Ƿǰ󶨵�: onCreate() --> onStartCommand() --> onDestory();
    onStartCommand()�������滻onStart()�����ģ��ȸ轨�������·���onStartCommand(),�������ȥ�鿴Դ�룬�ᷢ����ʵonStartCommand()����Ҳ�ǵ���onStart()�ġ�
�ұ��ǰ󶨵�: onCreate() --> onBind() --> onUnbind() --> onDestory();
ͬActivity��onCreate()����ֻ�ᱻ����һ�Ρ���onStartCommand()�������Ա����ö�Σ�onBind()�ȷ���Ҳֻ�ܵ���һ�Σ�����˵������onStartCommand()�����⣬����������һ������������ֻ�ܱ�����һ�Ρ�

####������˵˵�Ƚϸ��ӵģ����ֻ�����á�