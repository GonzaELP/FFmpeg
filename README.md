FFmpeg README
=============
## Como Compilarlo

1) Clonar el repositorio en la ruta deseada.

2) Instalar las dependencias:
```
sudo apt-get update -qq && sudo apt-get -y install \
  autoconf \
  automake \
  build-essential \
  cmake \
  git-core \
  libass-dev \
  libfreetype6-dev \
  libgnutls28-dev \
  libsdl2-dev \
  libtool \
  libva-dev \
  libvdpau-dev \
  libvorbis-dev \
  libxcb1-dev \
  libxcb-shm0-dev \
  libxcb-xfixes0-dev \
  meson \
  ninja-build \
  pkg-config \
  texinfo \
  wget \
  yasm \
  zlib1g-dev
```
3) Configurar, y compilar

```
./configure --enable-gnutls --enable-gpl --enable-libx264
make
```


## Ejemplos de funcionalidades agregadas.

1) Para agregar un tag genérico en el m3u8, se usa el flag `hls_add_tag`

```
./ffmpeg -i input -c copy -hls_add_tag "ALGUN TAG" out.m3u8
```

2) Para generar thumbnails de cada segmento, se usa el flag `hls_gen_thumbnails` en 1 
```
./ffmpeg -i input -c copy -hls_gen_thumbnails 1 out.m3u8
```
