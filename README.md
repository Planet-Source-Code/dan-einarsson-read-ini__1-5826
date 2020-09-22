<div align="center">

## Read INI


</div>

### Description

Opens a INI-file and Get the value of ex: "Screensaver=" without using any system calls!!!
 
### More Info
 
x = ReadINI("screensaver", "c:\windows\system.ini")

'or what ever

the value of the keyname

in this ex it would be perhaps: screensav.exe


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Dan Einarsson](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/dan-einarsson.md)
**Level**          |Intermediate
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/dan-einarsson-read-ini__1-5826/archive/master.zip)

### API Declarations

NONE that is why i posted it!!!


### Source Code

```
Function ReadINI(keyname As String, filename As String) As String
Open filename For Input Access Read As 1
Do Until EOF(1)
  Line Input #1, stemp
    ipos = InStr(stemp, keyname & "=")
    If ipos Then
      strinnick = strinnick + stemp
      ifound = True
      Allofit$ = strinnick
      wow$ = Mid(Allofit$, Len(keyname) + 2)
      GetINI = wow$
      Close 1
      Exit Function
    End If
Loop
  Close 1
End Function
'Written by: Dan Einarsson
```

