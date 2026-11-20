# xiaomi-pad-5-nabu-original-keyboard-fix

root化されていないROM(例えばcrDroid)ではテストしていません

### 事前準備
rootを獲ったばかりでXiaomi純正キーボードが動かない場合は次を試してください
```bash
echo "enable_keyboard" > /sys/bus/platform/drivers/xiaomi-keyboard/soc:xiaomi_keyboard/xiaomi_keyboard_conn_status
```
