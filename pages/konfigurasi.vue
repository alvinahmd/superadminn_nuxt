<template>
  <div>
    <navbar1 />
    <div class="flex flex-row">
      <div class="sticky top-40 left-0 z-40 w-24 h-full sm:translate-x-0" :class="{'w-64': !minimize}">
        <div class="h-screen py-4 overflow-y-auto bg-white shadow-md rounded-tr-3xl">
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
                    <img src="pengelola.png" alt="">
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
                    <img src="setting2.svg" alt="" class="pl-2">
                  </div>
                  <p v-if="!minimize" style="color: rgba(0, 117, 255, 1)">
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
      <div class="flex flex-row" :class="{'w-full': minimize}">
        <div class="px-8 py-4">
          <div class="bg-white shadow-lg h-full w-96">
            <div class="px-4 py-4">
              <h1 class="font-medium text-lg" style="color: rgba(68, 68, 68, 1)">
                Tanggal Hari Libur
              </h1>
              <div class="py-4">
                <date-picker v-model="time1" value-type="format" />
              </div>
              <div class="py-4">
                <h1 class="font-medium text-lg" style="color: rgba(68, 68, 68, 1)">
                  Keterangan Hari Libur
                </h1>
                <div class="pt-4">
                  <input type="text" class="w-60 px-2 py-2 rounded focus:outline-none focus:border-blue-500 focus:border-2" style="background-color: rgba(243, 243, 243, 1);">
                </div>
                <div class="flex justify-end translate-y-80">
                  <button class=" rounded text-white font-semibold text-sm w-24 text-center py-2" style="background-color: rgba(0, 117, 255, 1)">
                    Kirim
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="px-4 py-4" :class="{'w-full': minimize}">
          <div class="bg-white shadow-lg h-full w-full">
            <div class="px-4 py-4">
              <table class="items-center w-96 border" :class="{'w-full': minimize}">
                <thead>
                  <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(0, 117, 255, 1)">
                    <th class="py-4 px-12">
                      No
                    </th>
                    <th class="px-12">
                      Keterangan Libur
                    </th>
                    <th class="px-12">
                      Tanggal
                    </th>
                    <th class="px-12">
                      Action
                    </th>
                  </tr>
                </thead>
                <tbody class="w-full">
                  <tr class="border-b py-4">
                    <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                      1
                    </td>
                    <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                      Libur Hari Nyepi
                    </td>
                    <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                      <p>
                        29/3/2023
                      </p>
                    </td>
                    <td class="flex gap-2 translate-y-3 justify-center">
                      <img src="sampah.svg">
                      <img src="pensil.svg">
                    </td>
                  </tr>
                  <tr class="border-b py-4">
                    <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                      1
                    </td>
                    <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                      Libur Hari Nyepi
                    </td>
                    <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                      <p>
                        29/3/2023
                      </p>
                    </td>
                    <td class="flex gap-2 translate-y-3 justify-center">
                      <img src="sampah.svg">
                      <img src="pensil.svg">
                    </td>
                  </tr>
                  <tr class="border-b py-4">
                    <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                      1
                    </td>
                    <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                      Libur Hari Nyepi
                    </td>
                    <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                      <p>
                        29/3/2023
                      </p>
                    </td>
                    <td class="flex gap-2 translate-y-3 justify-center">
                      <img src="sampah.svg">
                      <img src="pensil.svg">
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      time1: null,
      minimize: null
    }
  }
}
</script>
