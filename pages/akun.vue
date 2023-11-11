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
            <a href="/beranda">
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
                    <img src="akun2.svg" alt="" class="pl-2">
                  </div>
                  <p v-if="!minimize" style="color: rgba(0, 117, 255, 1)">
                    Akun
                  </p>
                </div>
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class="w-full my-4 lg:my-0 md:mx-4">
        <div class="flex flex-col">
          <div class="bg-white flex flex-col-reverse md:flex-row w-full shadow-lg">
            <div class="flex md:flex-grow flex-col py-6 px-6">
              <div class="text-xl text-neutral-darkness mb-2">
                Akun
              </div>
              <div claSS="flex justify-between">
                <p class="text-gray-500 mt-1">
                  Semua informasi akunmu ada disini
                </p>
              </div>
              <div class="flex flex-row">
                <div class="relative">
                  <p class="mt-4 text-gray-600">
                    Foto
                  </p>
                  <img src="/profil.svg" class="mb-4 w-22 h-16 px-8">
                </div>
                <div class="mt-4 pl-8">
                  <div>
                    <div class="mb-4 pl-1 text-gray-600">
                      Nama Depan
                    </div>
                    <h1 class="w-64 px-4 py-2 mb-4 text-black rounded-lg" style="background-color: rgba(244, 251, 255, 1);">
                      {{ $nuxt.$cookiz.get('auth').user.first_name }}
                    </h1>
                    <div class="mb-4 pl-1 text-gray-600">
                      ID
                    </div>
                    <h1 class="w-64 px-4 py-2 mb-4 text-black rounded-lg" style="background-color: rgba(244, 251, 255, 1);">
                      {{ $nuxt.$cookiz.get('auth').user.id_user }}
                    </h1>
                    <div class="mb-4 pl-1 text-gray-600">
                      Admin ID
                    </div>
                    <h1 class="w-64 px-4 py-2 mb-4 text-black rounded-lg" style="background-color: rgba(244, 251, 255, 1);">
                      {{ $nuxt.$cookiz.get('auth').user.id_user }}
                    </h1>
                    <div class="mb-4 pl-1 text-gray-600">
                      Gender
                    </div>
                    <h1 class="w-64 px-4 py-2 mb-4 text-black rounded-lg" style="background-color: rgba(244, 251, 255, 1);">
                      {{ $nuxt.$cookiz.get('auth').user.gender }}
                    </h1>
                  </div>
                </div>
                <div class="mt-4 pl-8">
                  <div>
                    <div class="mb-4 pl-1 text-gray-600">
                      Nama Belakang
                    </div>
                    <h1 class="w-64 px-4 py-2 mb-4 text-black rounded-lg" style="background-color: rgba(244, 251, 255, 1);">
                      {{ $nuxt.$cookiz.get('auth').user.last_name }}
                    </h1>
                    <div class="mb-4 pl-1 text-gray-600">
                      Jabatan
                    </div>
                    <h1 class="w-64 px-4 py-2 mb-4 text-black rounded-lg" style="background-color: rgba(244, 251, 255, 1);">
                      {{ $nuxt.$cookiz.get('auth').user.job }}
                    </h1>
                    <div class="mb-4 pl-1 text-gray-600">
                      Passion
                    </div>
                    <h1 class="w-64 px-4 py-2 mb-4 text-black rounded-lg" style="background-color: rgba(244, 251, 255, 1);">
                      {{ $nuxt.$cookiz.get('auth').user.position }}
                    </h1>
                    <div class="mb-4 pl-1 text-gray-600">
                      Email
                    </div>
                    <h1 class="w-64 px-4 py-2 mb-4 text-black rounded-lg" style="background-color: rgba(244, 251, 255, 1);">
                      {{ $nuxt.$cookiz.get('auth').user.email }}
                    </h1>
                  </div>
                </div>
              </div>
              <div class="flex justify-end" @click="logout">
                <img src="/logout.svg">
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
      persik: null,
      minimize: null
    }
  },
  mounted () {
    this.getData()
  },
  methods: {
    // eslint-disable-next-line require-await
    async logout () {
      this.$router.replace('/')
      this.$toast.error(' Log out berhasil')
      this.nuxt.$cookiz.removeAll()
    },
    async getData () {
      try {
        await this.$axios.$get('https://7cec-2001-448a-5040-7137-e9c6-1add-fbea-123a.ngrok-free.app/api/users/' + this.$nuxt.$cookiz.get('auth').user.id, {
          headers: { 'ngrok-skip-browser-warning': '123123' }
        })
          .then((res) => {
          })
      } catch (error) {
        alert(alert.response.data.message)
      }
    }
  }
}
</script>
