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
      <div class="flex flex-col w-full">
        <div class="px-8 py-4">
          <div class="bg-white w-full h-full rounded-lg shadow-md">
            <div class="px-12 py-4">
              <div class="flex gap-4">
                <h1 class="text-base pt-4 font-normal" style="color: rgba(68, 68, 68, 1)">
                  Tampilkan
                </h1>
                <div class="pt-4">
                  <v-select v-model="perPage" :options="['1','2','3','4','5','6','7','8','9','10']" />
                </div>
                <h1 class="pt-4 font-normal" style="color: rgba(68, 68, 68, 1)">
                  user
                </h1>
              </div>
              <div class="flex justify-end -translate-y-12 pt-4">
                <div>
                  <input v-model="cari" type="search" placeholder="Cari Id,Nama,dan Lainnya" class="text-sm text-blue-200 font-medium border border-blue-100 w-56 rounded-md py-2 px-2 transition-all ease-in-out focus:outline-none focus:shadow-outline focus:outline-blue-300 focus:border-none placeholder:text-blue-200" @keyup.enter="getData">
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
                      <th>Check In</th>
                      <th>Check Out</th>
                      <th>Status</th>
                      <th>Detail</th>
                    </tr>
                  </thead>
                  <tbody class="w-full">
                    <tr v-for="(absen, index) in absensii" :key="index" class="border-b py-4">
                      <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                        {{ absen.id }}
                      </td>
                      <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                        {{ absen.first_name }} {{ absen.last_name }}
                      </td>
                      <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                        <p>
                          ID: {{ absen.id_user }}
                        </p>
                        <p>
                          {{ absen.email }}
                        </p>
                      </td>
                      <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                        <p>
                          <!-- {{ (absen.presence__user) ? absen.presence__user.presence__user__detail [1].presence_at : null }} -->
                        </p>
                      </td>
                      <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                        <p>
                          <!-- {{ (absen.presence__user) ? absen.presence__user.presence__user__detail [0].presence_at : null }} -->
                        </p>
                      </td>
                      <td class="items-center py-4 text-center text-sm">
                        <div class="w-14 h-9 rounded-lg mx-auto" style="background-color: rgba(206, 255, 211, 1)">
                          <p class="text-center py-2 font-semibold text-sm" style="color: rgba(0, 255, 25, 1)">
                            <!-- {{ (absen.presence__user) ? absen.presence__user.presence__user__detail[2].description : null }} -->
                          </p>
                        </div>
                      </td>
                      <td class="items-center py-4 text-center text-sm">
                        <div>
                          <a href="/detailabsen">
                            <p class="font-semibold underline underline-offset-1" style="color: rgba(0, 117, 255, 1)">
                              Detail
                            </p>
                          </a>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
              <div class="pt-4">
                <div class="flex justify-between">
                  <p class="font-semibold text-sm" style="color: rgba(156, 156, 156, 1)">
                    Menunjukan 1-9 Dari 49
                  </p>
                  <nav>
                    <ul class="flex gap-2">
                      <!-- Previous page item with disabled pointer events -->
                      <li>
                        <div class="rounded w-11 h-8 text-sm items-center" style="background-color: rgba(237, 237, 237, 1)">
                          <div class="item-center flex py-2 justify-center">
                            <svg width="8" height="15" viewBox="0 0 8 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                              <path d="M7 1L2 7.21739L7 14" stroke="#B9B9B9" stroke-width="2" stroke-linecap="round" />
                            </svg>
                          </div>
                        </div>
                      </li>
                      <!-- Page number 1 item -->
                      <li>
                        <div class="relative block rounded bg-transparent w-6 h-8 text-sm" style="background-color: rgba(237, 237, 237, 1)">
                          <div class="item-center flex py-2 justify-center">
                            <p class="font-semibold text-sm" style="color: rgba(185, 185, 185, 1)">
                              1
                            </p>
                          </div>
                        </div>
                      </li>
                      <!-- Current page (2) item with highlighted background and "current" label -->
                      <li>
                        <div class="relative block rounded bg-transparent w-6 h-8 text-sm" style="background-color: rgba(237, 237, 237, 1)">
                          <div class="item-center flex py-2 justify-center">
                            <p class="font-semibold text-sm" style="color: rgba(185, 185, 185, 1)">
                              2
                            </p>
                          </div>
                        </div>
                      </li>
                      <!-- Page number 3 item -->
                      <li>
                        <div class="relative block rounded bg-transparent w-6 h-8 text-sm" style="background-color: rgba(237, 237, 237, 1)">
                          <div class="item-center flex py-2 justify-center">
                            <p class="font-semibold text-sm" style="color: rgba(185, 185, 185, 1)">
                              3
                            </p>
                          </div>
                        </div>
                      </li>
                      <li>
                        <div class="relative block rounded bg-transparent w-6 h-8 text-sm" style="background-color: rgba(237, 237, 237, 1)">
                          <div class="item-center flex py-2 justify-center">
                            <p class="font-semibold text-sm" style="color: rgba(185, 185, 185, 1)">
                              4
                            </p>
                          </div>
                        </div>
                      </li>
                      <li>
                        <div class="relative block rounded bg-transparent w-6 h-8 text-sm" style="background-color: rgba(237, 237, 237, 1)">
                          <div class="item-center flex py-2 justify-center">
                            <p class="font-semibold text-sm" style="color: rgba(185, 185, 185, 1)">
                              5
                            </p>
                          </div>
                        </div>
                      </li>
                      <!-- Next page item -->
                      <li>
                        <div class="rounded w-11 h-8 text-sm items-center" style="background-color: rgba(237, 237, 237, 1)">
                          <div class="item-center flex py-2 justify-center">
                            <svg width="8" height="15" viewBox="0 0 8 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                              <path d="M1 14L6 7.78261L1 1" stroke="#0075FF" stroke-width="2" stroke-linecap="round" />
                            </svg>
                          </div>
                        </div>
                      </li>
                    </ul>
                  </nav>
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
  data () {
    return {
      minimize: null,
      absensii: null,
      cari: null,
      perPage: null
    }
  },
  watch: {
    perPage (val) {
      if (val) {
        this.getData()
      }
    }
  },
  mounted () {
    this.getData()
  },
  methods: {
    async getData () {
      try {
        await this.$axios.$get('https://7fcf-2001-448a-5040-6858-95a1-522a-aa10-7a83.ngrok-free.app/api/absensi', {
          headers: { 'ngrok-skip-browser-warning': '123123' },
          params: {
            cari: this.cari,
            perPage: this.perPage
          }
        })
          .then((res) => {
            this.absensii = res.message.data
          })
      } catch (error) {
        alert(alert.response.data.message)
      }
    }
  }
}
</script>
