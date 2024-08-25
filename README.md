# dicas_maravilhosas
Compilado de várias dicas e scripts úteis


# scripts

## editando videos via linha de comando ffmpeg

### juntando videos
 - liste os arquivos desejados para um arquivo texto:
   - ```bash
       printf "file '%s'\n" video1.mp4 video2.mp4 > list.txt
    ```
 - agora execute o ffmpeg para juntar os arquivos:
   - ```bash
      ffmpeg -f concat -i list.txt -c copy output.mp4
   ```

### cortando um trecho do video
 - neste exemplo, eu quero extrair o trecho do tempo 00h00m00s até 00h56m20s e salvá-lo como video2.mp4
   - ```bash
       ffmpeg -i input.mp4 -ss 00:00:00 -t 00:56:20 -c:v copy -c:a copy video2.mp4
     ```
