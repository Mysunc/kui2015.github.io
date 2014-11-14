---
layout: post
title: Android֮�ã��ģ� -- Intent
category: Android
tags: [Android]
excerpt: >
  Intent��ֵ��
---

Intent��ֵ��
ע�⣺
        �����ݵ���Ҫimplement Serializable
        ���ܴ�Bitmap
ʵ�֣�
        CurrentActivity����

        ```java
        Intent intent = new Intent(CurrentActivity.this, ResultActivity.class);
        Bundle bundle = new Bundle();
        intent.putSerializable("���key", �����ݶ����ʵ��);
        intent.putExtras(bundle);
        startActivity(intent);
        ```

        ResultActivity����
        ```java
        �����ݶ����ʵ�� = (��������)getIntent.getSerialzable("key");
        ```