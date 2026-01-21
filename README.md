<div align="center">

<h1>Cog Worker Skeleton</h1>

Easily convert cog based images to a runpod serverless worker.

</div>

## 使用方法

### 前提条件
确保您已经在本地构建好基础镜像，例如：
```bash
cog build -t user_id/image_name:tag
```

### 构建 Worker 镜像
使用本地已构建的镜像作为基础镜像：
```bash
docker build \
  --build-arg BASE_IMAGE=user_id/image_name:tag \
  -t user/cog-worker:latest \
  .
```

### 参数说明
- `BASE_IMAGE`: 本地已构建的基础镜像名称和标签（必需）
