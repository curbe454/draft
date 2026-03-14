# Here I notes a lot of mess. Below the are contents.

## LaTeX: minted style

<https://pygments.org/styles>

Italic commented style in minted may turn `$` into `£` which is awful for `shell scripts`.

igor,

Day non-italic comment style: staroffice,xcode,arduino,colorful,pastie,vs,perldoc,paraiso-light;  
in which I'd like `colorful,pastie` because they're colorful. But the string have been set background color, which is not good for shellscript. May xcode is better.

## Use MSVC in VS Code

It is not explicitly mentioned in the [official doc](https://code.visualstudio.com/docs/cpp/config-msvc#_run-vs-code-outside-the-developer-command-prompt), but it's waste of time to run `VsDevCmd.bat` each time when build.

```bat msvcode.bat
@echo off
call "D:\Microsoft Visual Studio\18\Community\Common7\Tools\VsDevCmd.bat" -arch=x64 -host_arch=x64
if errorlevel 1 (
    echo VsDevCmd.bat failed.
    pause
    exit /B 1
)

start "" code.exe %*
```

I save the above as `msvcode.bat` and config it into environment variable `PATH`.
