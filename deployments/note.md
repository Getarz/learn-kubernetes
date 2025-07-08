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

## rollout

ดู history deployment

```bash
kubectl rollout history deployment nginx-deployment
```

ย้อนกลับ version deployment ก่อนหน้า

```bash
kubectl rollout undo deployment nginx-deployment
```

## annotate

สร้าง description ใหเ deployment

```bash
kubectl annotate deployment nginx-deployment 'kubernetes.io/change-cause'='updated nginx deployment to version 1.27.1-alpine'
```

## scale

เพิ่มหรือลด resource แต่เป็นแบบชั่วคราว ถ้ามีการ apply ใหม่มันจะอีปเดตค่าจากไฟล์แทน

```bash
kubectl scale deployment nginx-deployment --replicas=3
```
