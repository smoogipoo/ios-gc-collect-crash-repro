Replication:

1. Run Visual Studio with `MONO_GC_DEBUG=nursery-canaries`.
2. Compile and deploy to device.
3. Click the button.
4. If no crash, restart debugging.

On a crash, you should see the following output:

```
2020-02-19 09:48:30 Checking nursery canaries...
2020-02-19 09:48:30 Checking nursery canaries...
Launched application 'com.companyname.ios-crash' on 'smgi 11' with pid 1209
2020-02-19 09:48:32.028 ios_crash[1209:224115] Xamarin.iOS: IDE Port: 10000 Transport: USB
2020-02-19 09:48:32.105 ios_crash[1209:224115] Xamarin.iOS: Successfully received USB connection from the IDE on port 10000, fd: 4
2020-02-19 09:48:32.106 ios_crash[1209:224115] Xamarin.iOS: Processing: 'start debugger: sdb'
2020-02-19 09:48:32.106 ios_crash[1209:224109] Xamarin.iOS: Debugger loaded with custom transport (fd: 4)
2020-02-19 09:48:32.107 ios_crash[1209:224115] Xamarin.iOS: Successfully received USB connection from the IDE on port 10000, fd: 5
2020-02-19 09:48:32.107 ios_crash[1209:224115] Xamarin.iOS: Processing: 'connect output'
2020-02-19 09:48:32.108 ios_crash[1209:224115] Xamarin.iOS: Successfully received USB connection from the IDE on port 10000, fd: 6
2020-02-19 09:48:32.109 ios_crash[1209:224115] Xamarin.iOS: Processing: 'start profiler: no'
2020-02-19 09:48:32.109 ios_crash[1209:224109] Xamarin.iOS: Profiler not loaded (disabled)
Loaded assembly: /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/System.dll
Loaded assembly: /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/Xamarin.iOS.dll
2020-02-19 09:48:32.140 ios_crash[1209:224109] Xamarin.iOS: Skipping assembly registration for Xamarin.iOS since it's not needed (dynamic registration is not supported)
2020-02-19 09:48:32.141 ios_crash[1209:224109] Xamarin.iOS: Skipping assembly registration for ios_crash since it's not needed (dynamic registration is not supported)
Thread started:  #2
Loaded assembly: /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash.exe
2020-02-19 09:48:34.908 ios_crash[1209:224109] .

=================================================================
	Native Crash Reporting
=================================================================
Got a SIGSEGV while executing native code. This usually indicates
a fatal error in the mono runtime or one of the native libraries 
used by your application.
=================================================================

=================================================================
	Native stacktrace:
=================================================================
	0x1006cbc28 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x1006c26bc - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x1006cf78c - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x185403434 - /usr/lib/system/libsystem_platform.dylib : <redacted>
	0x1007addb4 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x1007af238 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x1007afe38 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x1007ad930 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x1007a9d40 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x1007aac68 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x10077f888 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x1005258b0 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x100525b34 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x1004dfd2c - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x100632440 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x1006d2b3c - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x100766734 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x100769c1c - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x1004dc4e8 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x1004de0f4 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x185410cc8 - /usr/lib/libobjc.A.dylib : <redacted>
	0x1897fe918 - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : <redacted>
	0x18920d380 - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : <redacted>
	0x18920d6f4 - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : <redacted>
	0x18920c704 - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : <redacted>
	0x18983978c - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : <redacted>
	0x18983aa7c - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : <redacted>
	0x189816600 - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : <redacted>
	0x189890a58 - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : <redacted>
	0x189893010 - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : <redacted>
	0x18988c194 - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : <redacted>
	0x185678108 - /System/Library/Frameworks/CoreFoundation.framework/CoreFoundation : <redacted>
	0x18567805c - /System/Library/Frameworks/CoreFoundation.framework/CoreFoundation : <redacted>
	0x1856777c8 - /System/Library/Frameworks/CoreFoundation.framework/CoreFoundation : <redacted>
	0x185672694 - /System/Library/Frameworks/CoreFoundation.framework/CoreFoundation : <redacted>
	0x185671f40 - /System/Library/Frameworks/CoreFoundation.framework/CoreFoundation : CFRunLoopRunSpecific
	0x18f902534 - /System/Library/PrivateFrameworks/GraphicsServices.framework/GraphicsServices : GSEventRunModal
	0x1897fd580 - /System/Library/PrivateFrameworks/UIKitCore.framework/UIKitCore : UIApplicationMain
	0x1006a128c - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x10068e130 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x10068e0b4 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x1004df5b0 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x100632440 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x1006d2b3c - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x100766734 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x10076b8f4 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : mono_pmip
	0x1006b75f8 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x10080b658 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : _Z9__isctypeim
	0x1004def98 - /private/var/containers/Bundle/Application/4DE7D0ED-F986-47DA-8DC5-43C3CF2187F9/ios_crash.app/ios_crash : (null)
	0x1854f0e18 - /usr/lib/system/libdyld.dylib : <redacted>

=================================================================
	Basic Fault Address Reporting
=================================================================
Memory around native instruction pointer (0x1007acdd4):0x1007acdc4  00 00 80 52 01 00 80 52 fd 7b c1 a8 c2 ff ff 17  ...R...R.{......
0x1007acdd4  08 04 40 f9 09 09 40 92 2a 01 7f b2 5f 0d 00 f1  ..@...@.*..._...
0x1007acde4  61 00 00 54 00 31 7d 92 c0 03 5f d6 1f 3d 00 f1  a..T.1}..._..=..
0x1007acdf4  c1 00 00 54 28 10 40 b9 08 79 1f 53 08 7d 40 93  ...T(.@..y.S.}@.

=================================================================
	Managed Stacktrace:
=================================================================
	  at <unknown> <0xffffffff>
	  at System.GC:InternalCollect <0x00007>
	  at System.GC:Collect <0x00013>
	  at ios_crash.ViewController:UIButton197_TouchUpInside <0x0009b>
	  at System.Object:runtime_invoke_dynamic <0x0010f>
	  at <unknown> <0xffffffff>
	  at UIKit.UIApplication:UIApplicationMain <0x00007>
	  at UIKit.UIApplication:Main <0x0002f>
	  at UIKit.UIApplication:Main <0x00043>
	  at ios_crash.Application:Main <0x0007f>
	  at System.Object:runtime_invoke_dynamic <0x0010f>
=================================================================
```
