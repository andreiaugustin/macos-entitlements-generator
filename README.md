# macos-entitlements-generator
A script that generates a .plist file containing macOS entitlements. Useful for those who code sign outside of Xcode.

```
Usage: ./generate_entitlements.sh [-h] -o <output file> [ENTITLEMENT OPTIONS...]
Options:
  -h, --help                              Display this help message
  -o <output file>                        Output file path (required)

  Sandbox application (https://developer.apple.com/documentation/security/app_sandbox)
  --sandbox                               Adds Sandbox entitlement

  Network access (https://developer.apple.com/documentation/security/app_sandbox#3111191)
  --network-client                        Adds network client entitlement
  --network-server                        Adds network server entitlement

  Hardware access (https://developer.apple.com/documentation/security/app_sandbox#3111186)
  --microphone                            Adds microphone entitlement
  --usb                                   Adds USB entitlement
  --print                                 Adds printing entitlement
  --bluetooth                             Adds Bluetooth entitlement

  File access entitlements (https://developer.apple.com/documentation/security/app_sandbox#3111192)
  --user-selected-ro                      Adds entitlement for read-only access to user-selected files
  --user-selected-rw                      Adds entitlement for read-write access to user-selected files
  --downloads-ro                          Adds entitlement for read-only access to Downloads folder
  --downloads-rw                          Adds entitlement for read-write access to Downloads folder
  --pictures-ro                           Adds entitlement for read-only access to Pictures folder
  --pictures-rw                           Adds entitlement for read-write access to Pictures folder
  --music-ro                              Adds entitlement for read-only access to Music folder
  --music-rw                              Adds entitlement for read-write access to Music folder
  --movies-ro                             Adds entitlement for read-only access to Movies folder
  --movies-rw                             Adds entitlement for read-write access to Movies folder

  Runtime exceptions (https://developer.apple.com/documentation/security/hardened_runtime#3111188)
  --allow-jit                             Adds entitlement that allows the app to create writable and
                                          executable memory using the MAP_JIT flag.
  --allow-unsigned-executable-memory      Adds entitlement that allows the app to create writable and
                                          executable memory without the restrictions imposed by using the MAP_JIT flag.
  --allow-dyld-env-vars                   Adds entitlement that enables dynamic linker environment variables,
                                          which you can use to inject code into your app’s process.
  --disable-library-validation            Adds entitlement that enables loading arbitrary plug-ins or
                                          frameworks without requiring code signing.
  --disable-executable-memory-protection  Adds entitlement that disables all code signing protections while
                                          launching an app, and during its execution.
  --debugger                              Adds entitlement that indicates whether the app is a debugger and may
                                          attach to other processes.

  Resource access : https://developer.apple.com/documentation/security/hardened_runtime#3111190
  --audio-input                           Adds audio input access entitlement
  --camera                                Adds camera access entitlement
  --location                              Adds location access entitlement
  --addressbook                           Adds address book access entitlement
  --calendars                             Adds calendar access entitlement
  --photos                                Adds read-write Photo library access entitlement
  --apple-events                          Adds Apple events entitlement
```
