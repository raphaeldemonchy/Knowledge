# 
Knowledge

# Start project

- Create Docker image from Dockerfile
```
$> sudo docker build -t myimage
```

- Start image
```
docker run --rm -p 8000:8000 myimage
```

- Supprimer tout les images docker 
```
Get-Process -Id <PID> | ForEach-Object { $_.Modules }
```