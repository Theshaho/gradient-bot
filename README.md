# Gradient network hang-up script

- Project address: [https://app.gradient.network/](https://app.gradient.network/signup?code=R32C3T)

- Purchase proxy IP: [https://app.proxy-cheap.com](https://app.proxy-cheap.com/r/GL1F3J)

- TG: <https://t.me/ubuntufornodes>

## Start with Docker

### Prepare proxy IP (optional) ( Not recomanded )

Save the proxy address to the `proxies.txt` file in the format:

> socks5://username:password@proxyhost:port

Then start the container:

```bash
docker run -d \
-e APP_USER=user@mail.com \
-e APP_PASS=password \
-v ./proxies.txt:/app/proxies.txt \
overtrue/gradient-bot
```

Note: Please replace the `proxies.txt` path with the correct path. If there is no proxy, you can leave it blank, or `cd` to the directory where `proxies.txt` is located before executing the docker run command.

## View the running log

```bash
docker ps
```
This command will list all containers, find the corresponding container ID (the value corresponding to the "CONTAINER ID" column), and then execute:

```bash
docker exec -it <container_id> pm2 logs
```

## Delete container

```bash
docker rm -f <container_id>
```

## Update version

```bash
# delete old container
docker rm -f <container_id>

# pull new image
docker pull overtrue/gradient-bot

# run new container
docker run -d -e APP_USER=<user@mail.com> -e APP_PASS='<password>' -v ./proxies.txt:/app/proxies.txt overtrue/gradient-bot
```

## Note

- ## Here is my address in case you want to donate:
   - TRC20: `TSdnrpGgnwMTyEshsLDxW153oseiReZbB7`
  - - ERC 20: `0xC75e4118c31d31Eb7c067c0F78c8F594A8889568`
  - SOLANA: `EBbY1GskRSgwJcN3cuUCaZqk5zzpsr7A6ku7yg4TCGJa`
  - TON: `UQBDGcI3N58FpL1uhe5qqDBtcsxVfbmsIZQEz03WBxr-fdCe`
