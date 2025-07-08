# Kubectl Command

## create

สร้าง Deployments จากไฟล์

```bash
kubectl create -f nginx-rs.yaml
```

## get

ดึงข้อมูล Deployments

```bash
kubectl get deploy
```

สามารถใส่ flag --watch เพื่อ monitor realtime ได้

## describe

ดึงข้อมูล Deployments

```bash
kubectl describe deployment nginx
```
