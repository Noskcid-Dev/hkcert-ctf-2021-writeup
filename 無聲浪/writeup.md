# 無聲浪

| Info | Value |
| :--- | :-----: |
| Categories | #☆☆☆☆☆ #FORENSICS |
| Score | 50 |
| Total Solve (Rate) | 234/240 (63.3%) |

## Original Description
> 像密碼 若無線索 只好留下困惑

_IEEE Transactions on Signal Processing, Vol.51, (no.4), pp.1020–33, 2003._

How to:
1. Google the description
2. Find the GitHub repository written by Microsoft and meet the description
3. Download the tool and extract the Hex from audio
4.Decode the Hex into ASCII characters
5. Profit

## Description (Updated)

> 像密碼 若無線索
> 只好留下困惑

_IEEE Transactions on Signal Processing, Vol.51, (no.4), pp.1020–33, 2003._

Walkthrough:

1. Google the description
2. Find the [GitHub repository](https://github.com/toots/microsoft-audio-watermarking) written by Microsoft 
3. Download the tool (repository) in zip
4. Extract the zip, for example, you extract the zip under `D:\Downloads`
5. Copy the audio file (`waterwave.wav`) to `D:\Download\microsoft-audio-watermarking-master\build\`
6. Open the command prompt and execute the following:
```
D:\Download\microsoft-audio-watermarking-master\build\detect2003.exe D:\Download\microsoft-audio-watermarking-master\build\watermark.wav
```
7. Record ass Hex decoded
7. Convert all Hex it into ASCII characters, there are many [online tools](https://www.binaryhexconverter.com/hex-to-ascii-text-converter) that can be used
8. Profit

有部分參賽者反應 Github 上的工具未能正常執行。請使用命令提示字元(cmd.exe)打開該程式。
There is some contester mentioned that the tool on Github cannot be executed normally. Please use command prompt (cmd.exe) to execute the program.

## School Solves
| Overall Order | School Order | Name | Solved at |
| :-: | :-: | :-: | :-: |
| 80 | 1 |  S0092 - Immaculate Heart of Mary College | 2021-11-12 23:13:21.051 |
| 126 | 2 |  S0091 - Immaculate Heart of Mary College | 2021-11-13 20:26:54.225 |
| 138 | 3 | S0090 - Immaculate Heart of Mary College | 2021-11-13 23:25:36.862 |
| - | - | S0096 - Immaculate Heart of Mary College | Unsolved |

Total: 3/4 (75%)

## Writeup
When we submit the flag, the updated description aren't there yet (yes damn challenge writer aka Byron should update it earlier right...)

We googled the description directly and find the [repository](https://github.com/toots/microsoft-audio-watermarking), downloaded and unzipped the file and when we find there are two exe file for us to use. `watermark2003.exe` is for watermarking the audio file, while `detect2003.exe` is to detect watermarks. Therefore we run the `detect2003.exe` in command promopt (cmd) with the following command:
```
(Location of file)\microsoft-audio-watermarking-master\build\detect2003.exe (Location of file)\watermark.wav
```

It returns the output (only relavent part is listed below, information are neglected) listed in `output.txt` where total of 36 watermarks are detected. Copying the `WM` value of the watermarks, convert them to ASCII by the [ASCII Table](https://www.asciitable.com/) watermark by watermark and log them down in a spreadsheet as listed in `ascii.xlsx`. Finally, it returns us the flag.


## Flag
`hkcert21{w0rds_fr0m_3mpt1n3ss}`