# haconiwa-image-alpine

A haconiwa base image repository for alpine linux.

## Setting up

```ruby
Haconiwa.define do |config|
  root = Pathname.new("/var/lib/haconiwa/8cfccb3d")
  config.chroot_to root
  config.bootstrap do |b|
    b.strategy = "git"
    b.git_url = "https://github.com/haconiwa/haconiwa-image-alpine"
  end
  #...
end
```

Then

```
haconiwa create alpine.haco
```

## License

Assumed GPL-v2(like busybox).
