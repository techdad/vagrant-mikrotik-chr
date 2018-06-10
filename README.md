# vagrant-mikrotik-chr
This is a quick vagrant box for the mikrotik CHR software router. It's based on their provided ova image.

To run this box we will need to set `config.ssh.password = false` to be able to provision it with `vagrant ssh -- -t "/ip address print ; /ip address print ; /quit"`

Currently work in proggress to do vanilla ssh provision instead of vagrant's scp script & execute ssh system.

```ruby
Vagrant.configure("2") do |config|
  config.vm.provider  "virtualbox"
  config.vm.box = "http://blob.xlw.be/mikrotik-chr-6.42.3.box"
  config.ssh.password = false
end
```

If you have any questions you can send me on frank monkeytail knarf be