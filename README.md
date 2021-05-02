# TRAEFIK COM TLS COMO INGRESS DO KUBERNETES
 
 Este projeto detalha como é feito deploy do Traefik um proxy reverso e balanceador de carga de código aberto no kubernetes para servir como **ingress controller** do mesmo. 

## Import seu certificado tls para um secret

 > kubectl create secret tls nome_secret_tls \
 >  --cert=path/to/cert/file \
 >  --key=path/to/key/file

*Obs.: Substitua o nome do seu secret com mesmo presente no seu arquivo yaml no paramentro **secretName***

## Realize o deploy informando o namespace

> kubectl apply -f ./ -n kube-system


*Obs.: Acesse o traefik com o **FQDN** definido no arquivo ingress_service.yaml*