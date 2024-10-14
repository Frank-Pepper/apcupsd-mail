
# apcupsd-mail

## 1. Edit main configuration file

```
sudo nano /etc/apcupsd/apcupsd.conf
```

### Find and edit

-   UPSCABLE,  UPSTYPE,  DEVICE

``` 
UPSCABLE usb
UPSTYPE usb
#DEVICE /dev/ttyS0
DEVICE
```

## 2. Edit /etc/default/apcupsd

```
sudo nano /etc/default/apcupsd
```

```
ISCONFIGURED=yes
```

## 3. Clone repository

```
git clone https://github.com/Frank-Pepper/apcupsd-mail.git
```

## 4. Copy template_vars to variables file and set your vars

```
MJ_APIKEY_PUBLIC=""
MJ_APIKEY_PRIVATE=""
RECIPIENT_MAIL=""
RECIPIENT_NAME=""
```

## 5. Install nginx to display your UPS stats on e.g. raspberrypi.local

```
sudo apt-get install nginx
```

## 6. Run deploy script

```
./deploy
```
