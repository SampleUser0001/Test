# Test
Test

## Gitlab作成

```
mkdir config
mkdir logs
mkdir data
docker run \
    --publish 443:443 --publish 80:80 \
    --name gitlab \
    --volume $pwd/config:/etc/gitlab \
    --volume $pwd/logs:/var/log/gitlab \
    --volume $pwd/data:/var/opt/gitlab \
    gitlab/gitlab-ce:latest
```

## リモートリポジトリ変更

```
git remote set-url origin http://<GitlabのIP>/root/test.git
```

## ミラー作成

```
git clone --mirror <リポジトリURL>
```

## 参考

- [Qiita:GitLab をインストールしよう! (Docker Image)](https://qiita.com/masakura/items/e29f1dd4794bcaf066ce)
