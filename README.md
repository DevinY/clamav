# 用免費的Clamav替自己的網站掃毒吧

一、在自己的電腦建立名稱為clamav的image，並且取得最新的病毒碼
<pre>
docker-compose build --no-cache
</pre>
如果您沒有安裝docker-compose，可以用下方指令，建立clamav的image。
<pre>
docker build -t clamav . -f Dockerfile-alpine
</pre>

二、指令貼到目錄，就能進行掃毒囉，
指令中加了--rm，執行完必容器會刪除，要使用最新的病毒碼，掃毒前請都要build一次新版本。
<pre>
docker run --rm -v ${PWD}:/scan clamav
</pre>

