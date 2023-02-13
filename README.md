# FFmpeg 5.1.1
<div style="display: inline">
<img src="https://icon-library.com/images/ffmpeg-icon/ffmpeg-icon-20.jpg" style="width: 20px; height: 20px;">
<img src="https://colab.research.google.com/img/colab_favicon_256px.png" style="width: 20px; height: 20px;">
<div>
Static FFmpeg 5.1.1 binary for Google Colab

### [=] Installation
1. Clone this repository
```
!git clone https://github.com/XniceCraft/ffmpeg-colab --depth 1
```
2. Change script permission to executable
```
!chmod +x ./ffmpeg-colab/install
```
3. Install with provided script
```
!./ffmpeg-colab/install
```
4. Done

After installation you can remove the folder.

### [=] External Library
* ffnvcodec 11.1.5.2
* libaom 3.5.0
* libass 0.17.0
* libbluray 1.3.3
* libdav1d 1.0.0
* libfdk-aac 2.0.2
* libfontconfig 2.14.1
* libfreetype 2.12.1
* libfribidi 1.0.12
* libgme 0.6.3
* libkvazaar 2.1.0
* libmp3lame 3.100~ (<a href="https://github.com/openstreamcaster/lame">custom</a>)
* libopencore 0.1.6
* libopenh264 2.3.1
* libopenjpeg 2.5.1
* libopus 1.3.1
* libshine 3.1.1
* libsoxr 0.1.3
* libsrt 1.5.1
* libsvtav1 1.3.0
* libtheora 1.1.1
* libvidstab 1.1.0
* libvmaf 2.3.1
* libvorbis 1.3.7
* libvpx 1.12.0
* libx264 (see <a href="https://code.videolan.org/videolan/x264/-/tree/stable">x264-stable</a> branch) 
* libx265 3.5
* libxvid 1.3.7
* libzimg 3.0.4
* openssl 1.1.1s
* zlib 1.2.13

NVENC and NVDEC are supported.

### [=] FFmpeg Configuration
```
./configure --prefix=/home/ffmpeg-builder/release --pkg-config-flags=--static --extra-libs=-lm --disable-doc --disable-htmlpages --disable-manpages --disable-podpages --disable-txtpages --disable-debug --disable-shared --disable-ffprobe --enable-static --enable-gpl --enable-version3 --enable-runtime-cpudetect --enable-avfilter --enable-filters --enable-nvenc --enable-nvdec --enable-cuvid --pkgconfigdir=/home/ffmpeg-builder/release/lib/pkgconfig --extra-cflags='-I/home/ffmpeg-builder/release/include -static -static-libstdc++ -static-libgcc ' --extra-ldflags='-L/home/ffmpeg-builder/release/lib -fstack-protector -static -static-libstdc++ -static-libgcc ' --extra-cxxflags='-static -static-libstdc++ -static-libgcc ' --extra-libs='-ldl -lrt -lpthread' --enable-ffnvcodec --enable-gmp --enable-libaom --enable-libass --enable-libbluray --enable-libdav1d --enable-libfdk-aac --enable-libfontconfig --enable-libfreetype --enable-libfribidi --enable-libgme --enable-libkvazaar --enable-libmp3lame --enable-libopencore_amrnb --enable-libopencore_amrwb --enable-libopenh264 --enable-libopenjpeg --enable-libopus --enable-libshine --enable-libsoxr --enable-libsrt --enable-libsvtav1 --enable-libtheora --enable-libvidstab --ld=g++ --enable-libvmaf --enable-libvorbis --enable-libvpx --enable-libx264 --enable-libx265 --enable-libxvid --enable-libzimg --enable-openssl --enable-zlib --enable-nonfree --extra-libs=-lpthread --enable-pthreads --extra-libs=-lgomp
```

### [=] Builder Script
https://github.com/XniceCraft/ffmpeg-builder

```
CFLAGS="-mtune=generic" python ffmpeg-builder.py --use-system-build-tools --use-nonfree-libs --static-ffmpeg --exclude-targets "ffmpeg-msys2-deps" --disable-ffplay --extra-ffmpeg-args="--enable-nvenc --enable-nvdec --enable-cuvid" --build
```

### [=] Credit
* <a href="https://aomedia.googlesource.com/aom/">libaom</a>
* <a href="https://github.com/libass/libass">libass</a>
* <a href="https://www.videolan.org/developers/libbluray.html">libbluray</a>
* <a href="https://code.videolan.org/videolan/dav1d">libdav1d</a>
* <a href="https://github.com/mstorsjo/fdk-aac">libfdk-aac</a>
* <a href="https://www.freedesktop.org/wiki/Software/fontconfig/">libfontconfig</a>
* <a href="http://freetype.org/">libfreetype</a>
* <a href="https://github.com/fribidi/fribidi">libfribidi</a>
* <a href="https://bitbucket.org/mpyne/game-music-emu/wiki/Home">libgme</a>
* <a href="https://github.com/ultravideo/kvazaar">libkvazaar</a>
* <a href="https://lame.sourceforge.io/">libmp3lame</a> <a href="https://github.com/openstreamcaster/lame">custom</a>
* <a href="https://sourceforge.net/projects/opencore-amr/">libopencore</a>
* <a href="https://github.com/cisco/openh264">libopenh264</a>
* <a href="https://www.openjpeg.org/">libopenjpeg</a>
* <a href="https://opus-codec.org/">libopus</a>
* <a href="https://github.com/toots/shine">libshine</a>
* <a href="https://github.com/chirlu/soxr">libsoxr</a>
* <a href="https://github.com/Haivision/srt">libsrt</a>
* <a href="https://gitlab.com/AOMediaCodec/SVT-AV1">libsvtav1</a>
* <a href="https://www.theora.org/">libtheora</a>
* <a href="https://github.com/georgmartius/vid.stab">libvidstab</a>
* <a href="https://github.com/Netflix/vmaf">libvmaf</a>
* <a href="https://xiph.org/vorbis/">libvorbis</a>
* <a href="https://chromium.googlesource.com/webm/libvpx">libvpx</a>
* <a href="https://www.videolan.org/developers/x264.html">libx264</a>
* <a href="https://bitbucket.org/multicoreware/x265_git/wiki/Home">libx265</a>
* <a href="https://www.xvid.com/">libxvid</a>
* <a href="https://github.com/sekrit-twc/zimg">libzimg</a>
* <a href="https://www.openssl.org/">openssl</a>
* <a href="https://www.zlib.net/">zlib</a>
