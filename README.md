# mangata node update
>Öncelikle [buradan](https://goerli.eigenlayer.xyz/) toplam stake miktarımızı en az 1 ETH olarak yükseltelim.

>Bence 'lido staked ether' stake etmek daha mantıklı çünkü daha ucuz. Onu da [şuradan](https://app.uniswap.org/swap) temin edebilirsiniz. Bu da kontrat adresi: 0x1643E812aE58766192Cf7D2Cf9567dF2C37e9B7F

```console
cd avs-operator-setup
docker compose down

# burada .env dosyasını yedekleyelim.
# İsterseniz 'nano .env' ile içindekileri kopyalayıp kendi bilgisayarınızda bir metin belgesine yapıştırın.
# Ya da mobaxterm,Winscp termius vs ile de direkt dosyayı kendi bilgisayarınıza alabilirsiniz.

git reset --hard

git pull

docker compose pull

docker compose down

nano .env
```
>Şimdi burada değiştimemiz gereken yerler var aşağıya yazıyorum hepsini.Bunların hepsini az önce kaydetmiştik.Aynı şekil doldurun.

>ETH_RPC_URL= 

>ETH_WS_URL=

>ECDSA_KEY_FILE_HOST=

>BLS_KEY_FILE_HOST=

>ECDSA_KEY_PASSWORD=

>BLS_KEY_PASSWORD=

>Ayrıca 'ETH_RPC_URL='nin https ile başlamasına dikkat edin çünkü .env dosyasında bunlar farklı şekilde kayıt edilmiş(en azından bende öyle)

>ctrl+x y enter yapıp çıktık.

>O iki rpc'yi de [buradan](https://app.infura.io/) temin etmiştik.Bence buradan tekrar bakıp yazmak daha iyi.

![Ekran görüntüsü 2024-03-02 175003](https://github.com/janjakrosso/mangata-node-update/assets/121451942/2a6a3dcf-3aba-4b48-92a0-4232074e8924)

Son hali bu şekilde.

```console
docker compose up -d

docker ps

docker logs -f <konteyner id>

```
Ardından loglar böyle gözükecek.

![Ekran görüntüsü 2024-03-02 170017](https://github.com/janjakrosso/mangata-node-update/assets/121451942/e58c263b-f08f-4a8b-9454-87eb4efc99dc)

Mangata kaynaklı hatalar da olabiliyor mangata discordu takip edebilirsiniz.
