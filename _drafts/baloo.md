


Baloo is the file indexing service for KDE

* cpu issues + disk space issues
System -> Search -> File Search -> Enable File Search

``` bash
$> balooctl indexSize
Actual Size: 465.11 MiB
Expected Size: 345.00 MiB

           PostingDB:      80.40 MiB    23.304 %
          PositionDB:     146.63 MiB    42.500 %
            DocTerms:      32.08 MiB     9.298 %
    DocFilenameTerms:       4.13 MiB     1.197 %
       DocXattrTerms:       4.00 KiB     0.001 %
              IdTree:     540.00 KiB     0.153 %
          IdFileName:       3.03 MiB     0.879 %
             DocTime:       1.57 MiB     0.456 %
             DocData:       9.15 MiB     2.652 %
   ContentIndexingDB:            0 B     0.000 %
         FailedIdsDB:            0 B     0.000 %
             MTimeDB:       1.26 MiB     0.366 %
```

This seems like a lot, but I have a lot of files .. particularly multimedia (.mp3, .ogg, .mp4) ... so I'm not sure.

If you are concerned about the space usage, you can use the config file to exclude stuff.

```bash
$> cat ~/.config/baloofilerc 
[General]
dbVersion=2
exclude filters=*.lo,ui_*.h,.histfile.*,conftest,*.ini,po,CMakeTmpQmake,*.faa,cmake_install.cmake,*~,nbproject,*.map,.npm,moc_*.cpp,CVS,.yarn,*.m4,*.aux,node_packages,*.fna,*.nvram,*.fq,.pch,*.o,CMakeFiles,config.status,.moc,Makefile.am,_darcs,*.po,*.fasta,*.elc,*.tmp,*.qrc,.hg,CMakeCache.txt,*.gb,*.fastq,*.rcore,*.vm*,.uic,*.swap,lzo,libtool,*.omf,*.qmlc,confstat,*.la,autom4te,*.jsc,*.csproj,__pycache__,*.a,CTestTestfile.cmake,*.pyo,*.gmo,.svn,confdefs.h,*.part,*.moc,*.rej,.git,*.pc,*.loT,node_modules,*.so,*.gbff,*.db,.yarn-cache,*.class,lost+found,CMakeTmp,.obj,litmain.sh,qrc_*.cpp,*.pyc,*.orig,*.init,.bzr,.xsession-errors*,core-dumps
exclude filters version=4
first run=false
```

Probably want to stop the service before editing the config.

``` bash
$> sudo balooctl status

$> sudo balooctl stop

$> sudo balooctl disable

$> vi ~/.config/baloofilerc

[General]
exclude folders[$e]=/FolderA/,/FolderB/

$> sudo balooctl enable
```


Further Info : 

https://www.reddit.com/r/kde/comments/arnnxg/baloo_file_getting_really_large/