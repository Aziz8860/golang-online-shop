# Online Shop Project
1. Jalankan docker untuk PostgreSQL

```
docker run --name postgresql -e POSTGRES_USER=user -e POSTGRES_PASSWORD=password -e POSTGRES_DB=database -d -p 5432:5432 postgres:16
```

2. Export environment variable dan secret yang dibutuhkan

```
export DB_URI=postgres://user:password@localhost:5432/database?sslmode=disable
export ADMIN_SECRET=secret
```

note: nambahin env ke terminal di golang:
export nama_variabel=value
cara makenya: os.Getenv("nama_variabel")
dengan catatan, hanya ada di terminal itu aja. Jadi kalo buka terminal baru harus export lagi. Kalo mau permanen bisa ditaro di bashrc. Namun, karena ini database jadi kita mau tetep private.

3. Jalankan program

```
go run main.go
```






