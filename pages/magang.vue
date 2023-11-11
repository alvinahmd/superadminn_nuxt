<template>
  <div>
    <navbar1 />
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
                    <img src="pengelola2.svg" alt="">
                  </div>
                  <p v-if="!minimize" style="color: rgba(0, 117, 255, 1)">
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
      <div class="flex flex-col w-full">
        <div class="px-8 py-4">
          <div class="bg-white w-full h-full rounded-lg shadow-md">
            <div class="px-12 py-4">
              <div class="flex gap-4 -translate-y-2">
                <div class="text-sm font-medium text-center">
                  <ul class="flex flex-wrap -mb-px">
                    <a href="/pengelolaowner">
                      <li class="cursor-pointer inline-block border-b-2 text-gray-200 border-gray-200 hover:border-gray-400 hover:bg-gray-300 hover:rounded-lg">
                        Owner
                      </li>
                    </a>
                    <a href="/magang" class="ml-2">
                      <li>
                        <div class="cursor-pointer mr-2 inline-block  text-blue-600 border-b-2 border-blue-500 hover:border-blue-400 hover:bg-blue-300 hover:rounded-lg">
                          Magang
                        </div>
                      </li>
                    </a>
                  </ul>
                </div>
              </div>
              <div class="flex justify-end -translate-y-12">
                <div class="pr-8">
                  <div class="flex">
                    <div class="w-40 h-8 rounded" style="background-color: rgba(0, 117, 255, 1)">
                      <div class="flex justify-center py-2">
                        <div class="translate-y-1">
                          <svg width="11" height="11" viewBox="0 0 11 11" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M9.7261 4.22695H6.77134V1.2739C6.77134 0.571118 6.20193 0 5.49915 0C4.79636 0 4.22524 0.571118 4.22524 1.2739V4.22695H1.27219C0.569408 4.22695 0 4.79807 0 5.50085C0 6.20364 0.569408 6.77476 1.27219 6.77476H4.22524V9.7261C4.22524 10.4289 4.79636 11 5.49915 11C6.20193 11 6.77134 10.4289 6.77134 9.7261V6.77476H9.7261C10.4289 6.77476 11 6.20364 11 5.50085C11 4.79807 10.4289 4.22695 9.7261 4.22695Z" fill="white" />
                          </svg>
                        </div>
                        <p class="text-sm font-medium pl-2 text-white">
                          Tambah Akun
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
                <div>
                  <input type="search" placeholder="Cari Id,Nama,dan Lainnya" class="text-sm text-blue-200 font-medium border border-blue-100 w-56 rounded-md py-2 px-2 transition-all ease-in-out focus:outline-none focus:shadow-outline focus:outline-blue-300 focus:border-none placeholder:text-blue-200">
                </div>
              </div>
              <div>
                <table class="items-center w-full border">
                  <thead>
                    <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(0, 117, 255, 1)">
                      <th class="py-4">
                        No
                      </th>
                      <th>Nama</th>
                      <th>Kontak</th>
                      <th>Detail</th>
                    </tr>
                  </thead>
                  <tbody class="w-full">
                    <tr class="border-b py-4">
                      <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                        1
                      </td>
                      <td class="items-center">
                        <h1 class="pt-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                          Alvin Top Ahmad Djaelani
                        </h1>
                        <p class="text-center font-semibold text-sm" style="color: rgba(147, 147, 147, 1)">
                          Magang
                        </p>
                      </td>
                      <td class="items-center font-semibold py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                        <p>
                          ID:23467
                        </p>
                        <p>
                          Alvintop@gmail.com
                        </p>
                        <p>
                          08884845979
                        </p>
                      </td>
                      <td class="items-center py-4 text-center text-sm">
                        <div>
                          <p class="font-semibold underline underline-offset-1" style="color: rgba(0, 117, 255, 1)">
                            Detail
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
