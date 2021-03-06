# Mengenal Docker dan Container

Kali ini saya akan membahas tentang Apa itu Container dan Docker.

## Container
Apa sih Container itu ? dalam bahasa kita mengartikan container sebagai wadah. Yup, kasarnya Container ini zadalah paket / aplikasi yang mengandalkan isolasi virtual untuk menjalankan aplikasi yang dapat menjalankan sistem operasi kernel secara simultan tanpa memerlukan mesin virtual (VMs).

![enter image description here](./assets/vm-container.jpeg)

Perbedaanya apa ?? bisa dilihat dari arsitektur gambar diatas bahwa pada virtual machines terdapat Hypervisor pada arsitekturnya dan blok VM terdiri dari app, file lib dan binary serta seluruh bagian guest operating system. Sedangkan pada arsitektur container terdapat docker engine yang digunakan untuk menjalankan docker container serta pada container itu terdiri dari app dan semua dependasinya.

## Docker
Docker adalah sebuah project open source yang ditujukan untuk developer atau sysadmin untuk membangun, mengemas, dan menjalankan aplikasi dimana pun di dalam sebuah container. Nah Tugas utama Docker sudah jelas, sebagai Aplikasi yang bisa memanajemen Container kita nantinya, mulai dari Membuat, menghapus sebuah Container atau Menjalankan, Memulai Ulang, Menghentikan Container.

Fungsi utama Docker adalah menyederhanakan konfigurasi yang dibangun berdasarkan teknologi container.

![enter image description here](./assets/docker-architecture.png)

### Docker Daemon
Docker daemon adalah sebuah service yang dijalankan di dalam host dalam Operating System (OS) kita. Fungsinya adalah membangun, mendistribusikan, dan menjalankan container docker.

### Docker Object
- Docker images adalah sebuah template yang bersifat read only. Template ini sebenarnya adalah sebuah OS atau OS yang telah diinstall berbagai aplikasi. Docker images berfungsi untuk membuat docker container, dengan hanya 1 docker images kita dapat membuat banyak docker container.
- Docker Container adalah paket / aplikasi yang mengandalkan isolasi virtual untuk menjalankan aplikasi yang dapat menjalankan sistem operasi kernel secara simultan tanpa memerlukan mesin virtual (VMs).

### Docker Registry
Tempat terpusat bagi tim Anda untuk mengelola image Docker.

## Instalasi
- Ubuntu
  ```
  sudo apt update
  sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  sudo apt-key fingerprint 0EBFCD88
  sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
  sudo apt update
  sudo apt install docker-ce docker-ce-cli containerd.io
  docker version
  ```
- Debian -> `https://docs.docker.com/engine/install/debian/`
- CentOS -> `https://docs.docker.com/engine/install/centos/`
- Windows -> `https://docs.docker.com/docker-for-windows/install/`
- Mac -> `https://docs.docker.com/docker-for-mac/install/`

## Refrensi
- https://docs.docker.com/
- https://docs.docker.com/engine/install/
- https://www.cloudmatika.co.id/blog-detail/perbedaan-antara-vm-virtual-machine-dengan-container
- https://medium.com/@viandwi24/belajar-docker-mengenal-apa-itu-docker-dan-container-container-vs-virtual-machine-3c20d7288224
- https://www.ekrut.com/media/mengenal-docker-dan-penggunaannya-seperti-apa-sih
