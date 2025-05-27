- https://wiki.lineageos.org/extracting_blobs_from_zips
- https://github.com/linux-msm/pil-squasher
- https://gitlab.com/sdm845-mainline/firmware-google-pixel3

```fish
for f in **.mdt
    set cpath (string shorten -c '' --max (math (string length --visible $f) - 4) $f)
    echo ../../pil-squasher/pil-squasher ../../firmware-converted/$cpath.mbn $f
end
```

