# @capacitor-mlkit/barcode-scanning (SPM)

Swift Package Manager (SPM) compatible fork of [@capacitor-mlkit/barcode-scanning](https://github.com/capawesome-team/capacitor-mlkit/tree/main/packages/barcode-scanning).

## Why this fork?

The official `@capacitor-mlkit/barcode-scanning` plugin only supports CocoaPods for iOS dependency management. Swift Package Manager (SPM) is not supported for the ML Kit SDK, see [this comment](https://github.com/googlesamples/mlkit/issues/180#issuecomment-1298964099).  
This fork uses SPM instead.

## Installation

```bash
npm install github:joseph-navant/capacitor-mlkit-barcode-scanning-spm
npx cap sync
```

### Xcode Build Settings

Add these linker flags in Xcode under `Build Settings > Other Linker Flags`:

- `-ObjC`
- `-all_load`

### Limitations

The underlying google-mlkit-swiftpm (https://github.com/d-date/google-mlkit-swiftpm) XCFrameworks only include:

- arm64 for real devices
- x86_64 for Intel Mac simulators
  Apple Silicon Mac simulators are not supported (missing arm64 for iphonesimulator). Real iOS devices work fine.

### Credits

- Original plugin by Robin Genz (https://github.com/robingenz) / capawesome-team (https://github.com/capawesome-team).
- Google MLKit for iOS in SPM by Daiki Matsudate (https://github.com/d-date).

### License

Apache-2.0
