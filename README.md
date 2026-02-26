
# DevOps Test GitOps Config

本倉庫存放 K8s 部署清單 (Manifests)，供 ArgoCD 進行監控與同步。

## Structure

- `/manifests`: 存放 Deployment, Service 等 YAML 檔案。

## Workflow

1. 當 `DevOps-test-service` 產生新 Image 後，CI 會自動更新此處的 Tag。
2. ArgoCD 偵測到變更，自動將新版本部署至集群。
