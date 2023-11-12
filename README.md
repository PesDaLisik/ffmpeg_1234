нструкция FFMPEG для тех кто никогда не использовал терминал

—Скачать ffmpeg.exe и перенести на рабочий стол

—Нажимаем сочетание WIN+R

—Вводим CMD

—В терминале вводим cd Desktop

—Копируем скрипт полностью, вставляем в терминал, дальше надо нажать кнопку HOME на клавиатуре для перехода к началу текста, стрелками долистать и стереть "Вход", далее перетащить файл в терминал - что бы записать его путь, тоже самое с выходным файлом, нажимаем кнопку END и переходим начало, стираем "выход" и дропаем наш входной файл немного переименовав его, я обычно пишу HEVC_ в начале названия
—После всего этого наша строка для конвертации готова и можно нажать ENTER для запуска

ffmpeg.exe -i "ВХОД" -pix_fmt yuv420p -c:a libopus -b:a 80k -vbr on -frame_duration 60 -application audio -apply_phase_inv 0 -vf "scale=960:540:flags=bicubic" -c:v libx265 -preset fast -bf 14 -refs 5 -g 600 -keyint_min 600 -qp 25 -qmin 25 -i_qfactor 1.0 -x265-params "lowpass-dct=1:weightb=0:slices=1:pmode=0:pme=0:wpp=1:frame-threads=1:sao=1:sao-non-deblock=1:rc-lookahead=250:me=hex:subme=0:rect=0:amp=0:early-skip=1:aq-mode=3:aq-strength=3.00:b-adapt=2:max-merge=5:fast-intra=1:rskip=1:tskip=1:splitrd-skip=1:psy-rd=0.00:psy-rdoq=0.00:cutree=0:scenecut=0:b-intra=0:rd=6:deblock=6,6:bframe-bias=100000:cbqpoffs=-2:crqpoffs=-2:open-gop=0" -f mp4 "ВЫХОД.mp4"

для 854x480
заменить параметры на
-vbr 3 
scale=854:480
