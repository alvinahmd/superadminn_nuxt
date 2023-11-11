<template>
  <div>
    <navbar />
    <div class="flex flex-row">
      <div>
        <div class="sticky top-40 left-0 z-40 w-24 h-screen sm:translate-x-0" :class="{'w-64': !minimize}">
          <div class="h-screen py-4 overflow-x-hidden bg-white shadow-md rounded-tr-3xl">
            <div class="pl-4 cursor-pointer transition-all" :class="{'flex justify-end': !minimize}">
              <img src="/mini.svg" @click="minimize = !minimize">
            </div>
            <div class="px-4">
              <a href="/">
                <div class="flex gap-4 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                  <div>
                    <img src="beranda2.svg" alt="" class="pl-2 w-6">
                  </div>
                  <p v-if="!minimize" style="color: rgba(118, 118, 118, 1)">
                    Beranda
                  </p>
                </div>
              </a>
              <div class="pt-4">
                <a href="/absensi">
                  <div class="flex gap-4 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                    <div>
                      <img src="absen.svg" alt="" class="pl-2 w-6">
                    </div>
                    <p v-if="!minimize" style="color: rgba(118, 118, 118, 1)">
                      Absensi
                    </p>
                  </div>
                </a>
              </div>
              <div class="pt-4">
                <a href="https://meet.google.com/pwg-zcyr-bcp">
                  <div class="flex gap-4 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                    <div>
                      <img src="meet.svg" alt="" class="pl-2">
                    </div>
                    <p v-if="!minimize" style="color: rgba(118, 118, 118, 1)">
                      Meet
                    </p>
                  </div>
                </a>
              </div>
              <div class="pt-4">
                <a href="/pengguna">
                  <div class="flex gap-2 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                    <div>
                      <img src="pengguna.svg" alt="" class="pl-2">
                    </div>
                    <p v-if="!minimize" style="color: rgba(118, 118, 118, 1)">
                      Penguna
                    </p>
                  </div>
                </a>
              </div>
              <div class="pt-4">
                <a href="/pengelolaowner">
                  <div class="flex gap-1 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                    <div>
                      <img src="pengelola.png" alt="" class="pl-2">
                    </div>
                    <p v-if="!minimize" style="color: rgba(118, 118, 118, 1)">
                      Pengelola
                    </p>
                  </div>
                </a>
              </div>
              <div class="pt-4">
                <a href="/konfigurasi">
                  <div class="flex gap-4 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                    <div>
                      <img src="setting.svg" alt="" class="pl-2">
                    </div>
                    <p v-if="!minimize" style="color: rgba(118, 118, 118, 1)">
                      Konfigurasi
                    </p>
                  </div>
                </a>
              </div>
              <div class="pt-4">
                <a href="/akun">
                  <div class="flex gap-4 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                    <div>
                      <img src="akun.svg" alt="" class="pl-2">
                    </div>
                    <p v-if="!minimize" style="color: rgba(118, 118, 118, 1)">
                      Akun
                    </p>
                  </div>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="flex flex-col w-full">
        <div class="px-8 py-4">
          <div class="bg-white w-full h-screen rounded-t-lg shadow-lg">
            <div class="relative">
              <div class="w-full px-12">
                <h1 class="font-semibold text-lg py-4" style="color: rgba(68, 68, 68, 1)">
                  Notifikasi
                </h1>
                <div class="w-full">
                  <div class="py-4">
                    <div class="w-full h-16 rounded-lg" style="background-color: rgba(251, 254, 255, 1);box-shadow: 0px 0px 4px 1px rgba(68, 68, 68, 0.1); box-shadow: 0px 0px 4px 1px rgba(236, 245, 255, 1);">
                      <div class="flex gap-4 px-2 py-2">
                        <div class="">
                          <img src="bunder.svg" alt="">
                        </div>
                        <div class="flex flex-col">
                          <h1 class="font-semibold text-lg" style="color: rgba(68, 68, 68, 1)">
                            Manggala Teknologi
                          </h1>
                          <p class="text-center font-semibold text-sm" style="color: rgba(147, 147, 147, 1)">
                            Fransciesco steinlie telah mendaftar akun baru.
                          </p>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="py-4">
                    <div class="w-full h-16 rounded-lg" style="background-color: rgba(251, 254, 255, 1);box-shadow: 0px 0px 4px 1px rgba(68, 68, 68, 0.1); box-shadow: 0px 0px 4px 1px rgba(236, 245, 255, 1);">
                      <div class="flex gap-4 px-2 py-2">
                        <div class="">
                          <img src="bunder.svg" alt="">
                        </div>
                        <div class="flex flex-col">
                          <h1 class="font-semibold text-lg" style="color: rgba(68, 68, 68, 1)">
                            Manggala Teknologi
                          </h1>
                          <p class="text-center font-semibold text-sm" style="color: rgba(147, 147, 147, 1)">
                            Fransciesco steinlie telah mendaftar akun baru.
                          </p>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'BarChart',
  data () {
    return {
      minimize: false
    }
  }
}
</script>
<style>
html {
  overflow-x: hidden;
}
</style>
