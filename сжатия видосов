скачиваешь ffmpeg и распаковываешь на рабочий стол. 

дальше запускаешь командную строку (cmd)
(можешь win + r и написать cmd .Крч ты понял)

потом в cmd пишешь "cd desk" нажимаешь таб 

скопируй этот текст,то что снизу и на место "ВХОД" перекидываешь файл, который надо сжать


ffmpeg.exe -i "ВХОД" -pix_fmt yuv420p -c:a libopus -b:a 80k -vbr on -frame_duration 60 -application audio -apply_phase_inv 0 -vf "scale=960:540:flags=bicubic" -c:v libx265 -preset fast -bf 14 -refs 5 -g 600 -keyint_min 600 -qp 25 -qmin 25 -i_qfactor 1.0 -x265-params "lowpass-dct=1:weightb=0:slices=1:pmode=0:pme=0:wpp=1:frame-threads=1:sao=1:sao-non-deblock=1:rc-lookahead=250:me=hex:subme=0:rect=0:amp=0:early-skip=1:aq-mode=3:aq-strength=3.00:b-adapt=2:max-merge=5:fast-intra=1:rskip=1:tskip=1:splitrd-skip=1:psy-rd=0.00:psy-rdoq=0.00:cutree=0:scenecut=0:b-intra=0:rd=6:deblock=6,6:bframe-bias=100000:cbqpoffs=-2:crqpoffs=-2:open-gop=0" -f mp4 "ВЫХОД.mp4"

"ВЫХОД" можешь не трогать, он будет записывать в ту же папку(на рабочий стол), где и ffmpeg


(в строке "scale" можешь написать 1920\1080 и тд, но чтобы не аморфное разрешение было) 

Да, хуевое качество, зато ~8мб за 1 минуту видео, в основном для тг сжимают, но кого это ебет
