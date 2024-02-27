Steps to build for iOS:

```
(((install xcode + open it and install ios/mac frameworks)))
(((install brew)))
brew install cmake ninja ruby
echo 'export PATH="/user/local/opt/ruby/bin:$PATH"' >> ~/.zshrc
sudo gem install cocoapods
mkdir -p /tmp/hermes/output
git clone git@github.com:ExodusMovement/hermes.git
cd hermes
./utils/build-ios-framework.sh
./utils/build-mac-framework.sh
tar -zcvf ios.tar.gz destroot
shasum -a 256 ios.tar.gz > ios.tar.gz.shasum
```
