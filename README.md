# xiaomi-pad-5-nabu-original-keyboard-fix
Xiaomi Pad 5純正キーボードでバッククオートを入力できない問題を修正します<br>
元々バックオートが至極入力しづらいキーボードです。ESCに`~`と共に同居しているからです<br>
このfixはGeneric.klをベースとしています
- テスト環境
  - crDroid 12(**rooted**)

root化されていないデバイスではテストしていません<br>
もしかするとadbやROMによってインジェクトできるかもしれませんが、**全くテストしていません**

### 事前準備
rootを獲ったばかりでXiaomi純正キーボードが動かない場合は次を試してください
```bash
echo "enable_keyboard" > /sys/bus/platform/drivers/xiaomi-keyboard/soc:xiaomi_keyboard/xiaomi_keyboard_conn_status
```
参考:https://github.com/Till0196/magisk-module-xiaomi-keyboard-nabu-fix/blob/main/post-fs-data.sh

# 使用方法
root権限のターミナルアプリから`mount -o rw,remount /`を実行後、Xiaomi_Pad.klを`/system/usr/keylayout/`と`data/system/devices/keylayout/`に置きrebootします

### example(Termux想定)
```bash
git clone https://github.com/Aechaa6lahh3ohp/xiaomi-pad-5-nabu-original-keyboard-fix/ mod ; cd mod
sudo -s
cp -v Xiaomi_Pad.kl /system/usr/keylayout/
cp -v Xiaomi_Pad.kl  /system/devices/keylayout/
reboot
```
