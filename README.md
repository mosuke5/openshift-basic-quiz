# OpenShift Basic Quiz
## クイズ
1. `container-quiz` Namespaceを作成する
2. そのNamespaceにhogeという名前のDeploymentを作成する。利用するコンテナイメージは、`nginxinc/nginx-unprivileged:latest` とする。
3. そのDeploymentの環境変数 `FOO=BAR`の値を設定する
4. そのDeploymentを公開するServiceとRouteを作成する（それぞれの名前は `hoge`とする）。   
5. `test-cm` という名前のConfigMapを作成する。ConfigMapの値は `cm-key=cm-value` とする
6. そのConfigMapをhogeという名前のDeploymentにマウントし、環境変数として設定する。
7. `test-secret` という名前のSecretを作成する。Secretの値は `secret-key=secret-value` とする
8. そのSecretをhogeという名前のDeploymentにマウントし、環境変数として設定する。
9. そのDeploymentのレプリカ数を３に変更する


## 実行方法
```
ansible-playbook check_openshift_resources.yml
```

### proxyが必要な場合
```
ansible-playbook check_openshift_resources.yml --extra-vars="proxy_url=http://xxxxxxxx"
```
