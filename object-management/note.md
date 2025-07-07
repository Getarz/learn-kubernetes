# Kubectl Command

## create

สร้าง resource จากไฟล์

```bash
kubectl create -f nginx-pod.yaml
```

## get

เราสามารถดู configuration ได้จาก flag -o yaml

```bash
kubectl get pod nginx-pod -o yaml
```

## delete

ลบ resource จากไฟล์

```bash
kubectl delete -f nginx-pod.yaml
```

หรือจะลบทั้งโฟลเดอร์ก็ได้

```bash
kubectl delete -f object-management
```

## replace

๕ือการเขียนทับ configuration แต่ก็จะไม่สามารถทำได้ในบางกรณี เช่น การเปลี่ยน image

```bash
kubectl replace -f nginx-pod.yaml
```

## apply

คือการอัปเดตค่า configuration

```bash
kubectl apply -f nginx-pod.yaml -f nginx-svc.yaml
```

หรือถ้าอยาก apply ทีเดียวทั้ง folder ก็ได้

```bash
kubectl apply -f object-management
```

## diff

เปรียบเทียบไฟล์ manifest เพื่อเช็คการเปลี่ยนแปลง

```bash
kubectl diff -f object-management
```
