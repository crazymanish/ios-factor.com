# ios-factor

Storing data and configuration according to Apple's guideline is crucial for your app's lifecycle, in particular when it comes to iCloud sync, upgrading to a new phone and restoring a phone from a backup.

[iOS Data Storage Guidelines](https://developer.apple.com/icloud/documentation/data-storage/index.html)

- `Documents`: Use this directory for user-generated content, it will be backed up
- `Caches`: Use this directory for data that can be regenerated
- `tmp`: Use this directory for temporary files
- Make use of the `do not back up` attribute

Never store sensitive user-information (like passwords or sessions) in those directories. Use the Keychain API, which comes with various advantages:

<!-- TODO: finish -->

## Open TODOs

- tooling like react native: how do you sync the native code with the JS code
- keychain and storing login

## How to contribute

To run the server locally:

- `git clone https://github.com/ios-factor/ios-factor.com`
- `bundle install`
- `bundle exec jekyll serve`
- Open [http://127.0.0.1:4000](http://127.0.0.1:4000)

## Disclaimer

This project is licensed under the terms of the MIT license. See the [LICENSE](LICENSE) file.

This project is in no way affiliated with Apple Inc or Google Inc. 
