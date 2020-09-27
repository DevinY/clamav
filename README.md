在自己的電腦建立名稱為clamav的image
並且取得最新的病毒碼

docker-compose build

指令貼到目錄，就能進行掃圖囉

docker run --rm -v ${PWD}:/scan clamav
# clamav
