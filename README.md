# Procyon

```bash
docker run -p 8080:8080 -p 9090:9090 procyon
```

```bash
./install-cli.sh
```

```bash
procyon-cli functions deploy \
  --wasm https://registry-cdn.wapm.io/contents/k33g/yo/1.0.0/yo.wasm \
  --function yo \
  --revision 1.0.0
```


```bash
procyon-cli functions call \
  --function yo \
  --revision 1.0.0 \
  --method POST \
  --data 'Jane Doe'
```
