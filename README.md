# Procyon Demo with Docker

## Install

> build the image
```bash
./build.sh
```

## Run Procyon

```bash
docker run -p 8080:8080 -p 9090:9090 -d  procyon
```

## Install the Procyon CLI

```bash
./install-cli.sh
```

## Test Procyon

> Deploy a function to Procyon (the Runnable is published on wapm):
```bash
procyon-cli functions deploy \
  --wasm https://registry-cdn.wapm.io/contents/k33g/yo/1.0.0/yo.wasm \
  --function yo \
  --revision 1.0.0
```

> Call the function:
```bash
procyon-cli functions call \
  --function yo \
  --revision 1.0.0 \
  --method POST \
  --data 'Jane Doe'
```

> Or:
```bash
curl http://localhost:8080/functions/yo/1.0.0 -d 'Jane Doe'
```
