FROM cgswong/vault

COPY vault-config.conf /root/vault.conf

ENTRYPOINT ["/usr/local/bin/vault", "server", "-config", "/root/vault.conf"]