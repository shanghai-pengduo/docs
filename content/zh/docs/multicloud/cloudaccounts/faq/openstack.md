---
title: "Openstack"
weight: 2
description: >
    Openstack 对接常见问题。
---

## 对接 Openstack 后端使用ceph 存储的时候，云账户管理，经常同步不下相关的ceph 磁盘配置

我们需要在创建磁盘的时候指定相关的ceph 类型。首先检查一下是否指定了volume_backend_name.

1、查看cinder配置文件的ceph 指定的name,没有就添加：

```
[ceph]
volume_driver = cinder.volume.drivers.rbd.RBDDriver
rbd_pool = volumes
rbd_ceph_conf = /etc/ceph/ceph.conf
rbd_flatten_volume_from_snapshot = false
rbd_max_clone_depth = 5
rbd_store_chunk_size = 4
rados_connect_timeout = -1
glance_api_version = 2
rbd_user = cinder
rbd_secret_uuid = f4f03912-7ec7-42e9-b9ea-8735217d8cc9
volume_backend_name = ceph
```

2、添加ceph类型关联到volume_backend_name:

```bash
[root@cinder1 cinder]# cinder extra-specs-list
[root@cinder1 cinder]# cinder type-create ceph
+--------------------------------------+------+-------------+-----------+
| ID                                   | Name | Description | Is_Public |
+--------------------------------------+------+-------------+-----------+
| 00103a9a-bcf6-4c25-afb4-fd2a211cc706 | ceph | -           | True      |
+--------------------------------------+------+-------------+-----------+
[root@cinder1 cinder]# cinder type-key ceph set volume_backend_name=ceph
[root@cinder1 cinder]# cinder extra-specs-list
+--------------------------------------+------+---------------------------------+
| ID                                   | Name | extra_specs                     |
+--------------------------------------+------+---------------------------------+
| 00103a9a-bcf6-4c25-afb4-fd2a211cc706 | ceph | {'volume_backend_name': 'ceph'} |
+--------------------------------------+------+---------------------------------+
```

3、重新添加volume；指定类型为ceph即可。

4、cloudpods可以重新同步，可以看到磁盘已经同步下来。
