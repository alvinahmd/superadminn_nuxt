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
              <a href="/meet">
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
                    <img src="pengguna2.svg" alt="" class="pl-2">
                  </div>
                  <p v-if="!minimize" style="color: rgba(0, 117, 255, 1)">
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
                <a href="/tambahakun">
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
                </a>
                <div>
                  <input v-model="cari" type="search" placeholder="Cari Disini" class="text-sm text-blue-200 font-medium border border-blue-100 w-56 rounded-md py-2 px-2 transition-all ease-in-out focus:outline-none focus:shadow-outline focus:outline-blue-300 focus:border-none placeholder:text-blue-200" @keyup.enter="getData">
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
                      <th>Passion</th>
                      <th>Active</th>
                      <th>Akun</th>
                      <th>Action</th>
                    </tr>
                  </thead>
                  <tbody class="w-full">
                    <tr v-for="(pengguna, index) in users" :key="index" class="border-b py-4">
                      <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                        {{ index+1 }}
                      </td>
                      <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                        {{ pengguna.first_name }} {{ pengguna.last_name }}
                      </td>
                      <td class="items-center font-semibold py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                        <p>
                          {{ pengguna.id_user }}
                        </p>
                        <p>
                          {{ pengguna.email }}
                        </p>
                      </td>
                      <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                        <div class="w-14 h-5 rounded-full" style="background: linear-gradient(90deg, #C4A7F4 0%, #B7B5F4 35.42%, #A8C8F5 63.02%, #95DEF7 100%);">
                          <p class="text-white font-semibold text-sm">
                            {{ pengguna.position }}
                          </p>
                        </div>
                      </td>
                      <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                        <p class="items-center font-semibold py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                          {{ pengguna.active }}
                        </p>
                      </td>
                      <td class="items-center py-4 text-center text-sm">
                        <div class="w-24 h-9 rounded-lg mx-auto" style="background-color: rgba(206, 255, 211, 1)">
                          <p class="text-center py-2 font-semibold text-sm px-2" style="color: rgba(0, 255, 25, 1)">
                            {{ pengguna.akun }}
                          </p>
                        </div>
                      </td>
                      <td class="flex gap-2 translate-y-3 py-4 justify-center">
                        <img src="sampah.svg" @click="hapus(pengguna.id)">
                        <nuxt-link :to="'/simpan/' + pengguna.id">
                          <img src="pensil.svg">
                        </nuxt-link>
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
      users: null,
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
    async hapus (id) {
      try {
        await this.$axios.$delete('https://7fcf-2001-448a-5040-6858-95a1-522a-aa10-7a83.ngrok-free.app/api/users/' + id, {
          headers: { 'ngrok-skip-browser-warning': '123123' }
        })
          .then((res) => {
            console.log('res', res)
            this.$router.replace('/pengguna')
            this.$toast.success('Hapus tiket berhasil')
          })
      } catch (error) {
        alert(error.response.data.message)
        console.log(error)
      }
    },
    async getData () {
      try {
        await this.$axios.$get('https://7fcf-2001-448a-5040-6858-95a1-522a-aa10-7a83.ngrok-free.app/api/users', {
          headers: { 'ngrok-skip-browser-warning': '123123' },
          params: {
            cari: this.cari,
            perPage: this.perPage
          }
        })
          .then((res) => {
            this.users = res.message.data
            // this.nuxt.$cookiz.removeAll()
          })
      } catch (error) {
        console.log(error)
        alert(error.response.data.message)
      }
    }
  }
}
</script>
