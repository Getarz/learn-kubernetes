# Kubectl Command

## create

สร้าง Replicaset จากไฟล์

```bash
kubectl create -f nginx-rs.yaml
```

## get

ดึงข้อมูล Replicaset

```bash
kubectl get rs
```

สามารถใส่ flag --watch เพื่อ monitor realtime ได้

## describe

ดึงข้อมูล Replicaset

```bash
kubectl describe rs nginx
```

! Caution

- ถ้าเกิดมีการเปลี่ยน image ใน spec ตอนที่ replica ทำงานอยู่แล้วเรา apply ตัว pod จะไม่ถูดแก่ไข จนกว่าจะมีการ delete แล้วจึงสร้าง pod ตัวใหม่ที่มีการอัปเดดเข้ามา
- ถ้ามีการสร้าง replicaset ใหม่โดยที่มีของเดิมอยู่แล้ว โดยที่ไม่สนว่าเป็ยของใตร ขอแค่ spec เหมือน มันก็จะนับรวมตัวนั้นเข้าไปใน replicaset ด้วย
