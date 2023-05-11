# gamedemo
gamedemo
#依次运行以下命令，安装jd_v4_bot和面板。


1、安装v4_bot(amd64) 一键命令（1）

  (提前在宿主机新建文件夹jd_v4_bot，下面再新建config,log,own,diy,scripts五个文件夹。如要自行修改路径，记得为绝对路径。)
  
  docker run -dit \
   -v /jd_v4_bot/config:/jd/config \
   -v /jd_v4_bot/log:/jd/log \
   -v /jd_v4_bot/own:/jd/own \
   -v /jd_v4_bot/diy:/jd/jbot/diy \
   -v /jd_v4_bot/scripts:/jd/scripts \
   -p 5678:5678 \
   -e ENABLE_HANGUP=true \
   -e ENABLE_WEB_PANEL=true \
   -e ENABLE_WEB_TTYD=true \
   --name jd_v4_bot \
   --hostname jd_v4_bot \
   --restart always \
   annyooo/jd:v4_bot
