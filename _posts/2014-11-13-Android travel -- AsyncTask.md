---
layout: post
title: Android֮�ã����� -- AsyncTask
category: Android
tags: [Android]
excerpt: >
  ������˵һ˵AsyncTask
---

������˵һ˵AsyncTask

####AsyncTask��ʵ��

1.����AsyncTask�����࣬Ϊ�������Ͳ���ָ�����ͣ��粻��Ҫ��Ϊvoid��
    ��������
        Params����������
        Progress������ֵ����
        Result������ֵ����
        
2.����ʵ��doInBackground()�������ɸ�����Ҫʵ��onProgressUpdate(),onPreExecute(),onPostExecute()��������Щ����ֻ����ϵͳ������á�
3.�����߳��е���AsyncTaskʵ����execute()������

####�����е�û��

���Ҫ��AsyncTask�����������UI���ɽ�Activity��Context��ʵ��������ʱ�����������ݹ�ȥ��
�����ҳ���������Σ�AsyncTask�Ὣ�µ�������뵽deque�У������쳣��

```java
	if(asyncTaskTest.getStatus() == AsyncTask.Status.RUNNING)
		asyncTaskTest.cancel(true);
```