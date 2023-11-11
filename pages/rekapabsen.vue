<template>
  <div>
    <div class="flex justify-between px-8 py-4">
      <div>
        <img src="logo.svg" alt="">
      </div>
      <div class="grid grid-cols-2 gap-4">
        <div>
          <img src="lonceng.svg" alt="">
        </div>
        <div>
          <img src="profil.svg" alt="">
        </div>
      </div>
    </div>
    <div class="flex flex-row w-full">
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
                    <img src="absen2.svg" alt="" class="pl-2 w-6">
                  </div>
                  <p v-if="!minimize" style="color: rgba(0, 117, 255, 1)">
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
      <div class="px-8 py-4">
        <div class="bg-white w-full h-full rounded-t-lg shadow-lg">
          <div class="px-12 py-4">
            <div>
              <h1 class="font-semibold text-lg pt-8" style="color: rgba(68, 68, 68, 1)">
                Rekap Absensi
              </h1>
              <div class="flex justify-between">
                <div class="w-60">
                  <v-select :options="['2022','2023','2024']" placeholder="Tahun" />
                </div>
                <button class="bg-blue-500 w-40 h-max rounded-md transition-all duration-300 hover:bg-opacity-70">
                  <div class="px-2 py-2 flex gap-2">
                    <div class="translate-y-1">
                      <img src="download.svg">
                    </div>
                    <p class="text-white font-semibold text-base">
                      Download PDF
                    </p>
                  </div>
                </button>
              </div>
              <div class="pt-8">
                <table class="items-center w-full border">
                  <thead>
                    <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(0, 117, 255, 1)">
                      <th class="py-4 px-4">
                        Tanggal
                      </th>
                      <th class="py-4 px-4">
                        Kontak
                      </th>
                      <th class="py-4 px-4">
                        Checkin
                      </th>
                      <th class="py-4 px-4">
                        Kegiatan
                      </th>
                      <th class="py-4 px-4">
                        Checkout
                      </th>
                      <th class="py-4 px-4">
                        Kegiatan
                      </th>
                      <th class="py-4 px-4">
                        Keterangan
                      </th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr class="border-b py-4">
                      <td class=" text-sm items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                        2/2/2023
                      </td>
                      <td class="text-sm items-center py-4 text-center font-semibold" style="color: rgba(126, 126, 126, 1)">
                        Pt.Manggala Teknologi,tegowangi,Kec.Pare,Kab,Kediri
                      </td>
                      <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                        07.45
                      </td>
                      <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                        Membuat Halaman Kata Sandi Membuat Es teh
                      </td>
                      <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                        ----
                      </td>
                      <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                        Membuat Halaman Kata Sandi Membuat Es teh
                      </td>
                      <td class="items-center py-4 text-center text-sm">
                        <div class="w-14 h-9 rounded-lg mx-auto" style="background-color: rgba(206, 255, 211, 1)">
                          <p class="text-center py-2 font-semibold text-sm" style="color: rgba(0, 255, 25, 1)">
                            Hadir
                          </p>
                        </div>
                      </td>
                    </tr>
                    <tr class="border-b py-4">
                      <td class=" text-sm items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                        2/2/2023
                      </td>
                      <td class="text-sm items-center py-4 text-center font-semibold" style="color: rgba(126, 126, 126, 1)">
                        Pt.Manggala Teknologi,tegowangi,Kec.Pare,Kab,Kediri
                      </td>
                      <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                        07.45
                      </td>
                      <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                        Membuat Halaman Kata Sandi Membuat Es teh
                      </td>
                      <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                        ----
                      </td>
                      <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                        Membuat Halaman Kata Sandi Membuat Es teh
                      </td>
                      <td class="items-center py-4 text-center text-sm">
                        <div class="w-24 h-9 rounded-lg mx-auto" style="background-color: rgba(255, 219, 220, 1)">
                          <p class="text-center py-2 font-semibold text-sm" style="color: rgba(255, 27, 34, 1)">
                            Tidak Hadir
                          </p>
                        </div>
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
  </div>
</template>
<script>
export default {
  data () {
    return {
      minimize: null
    }
  }
}
</script>
