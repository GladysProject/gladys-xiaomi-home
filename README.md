# gladys-xiaomi-home 

The goal of this module is to receive events from Xiaomi Home Devices

## Hardware

- [Xiaomi GateWay](https://fr.gearbest.com/living-appliances/pp_344667.html?wid=55)
- [Xiaomi Switch Button](https://fr.gearbest.com/smart-light-bulb/pp_257679.html?wid=55)
- [Xiaomi Door & Sensor](https://fr.gearbest.com/access-control/pp_626703.html?wid=55)
- [Xiaomi Aqara Humidity & Temperature](https://fr.gearbest.com/access-control/pp_626702.html?wid=55)

## Prerequisite

- Install the MiHome app from Google Play or AppStore
- Set your region to Mainland China when app init or under Settings -> Locale
- Setup, connect your Gateway & all your Xiaomi devices 
- Update gateway to the latest firmware
- Enable developer mode by following this tutoriel => https://github.com/fooxy/homeassistant-aqara/wiki/Enable-dev-mode

## Installation

Connect to your Raspberry Pi. 

Clone this repository : 

```
git clone https://github.com/GladysProject/gladys-xiaomi-home
```

Go the directory :

```
cd gladys-xiaomi-home
```

Install the dependencies : 

If you have yarn (pre-installed on Gladys Raspbian image), just do :

```
yarn install
```

If not, you can do :

```
npm install
```

You now need to modify the `config.js` file :

```
nano config.js
```

Edit each line with your configuration.

Then, execute :

```
pm2 start /home/pi/gladys-xiaomi-home/app.js --name gladys-xiaomi-home
```

So that gladys-xiaomi-home run in background :)

## Debug

To debug, you can see logs by calling : 

```
pm2 logs gladys-xiaomi-home
```