<template>
  <div>
    <div class="flex px-8 py-4 ">
      <div>
        <img src="/logo.svg">
      </div>
      <div class="items-center mx-auto pt-4">
        <div class="bg-white px-8 py-2 rounded-full shadow-lg text-center items-center">
          <p class="font-semibold">
            Hii,
            <span style="color: rgba(0, 117, 255, 1)">Diaz ibanez kaka</span>
          </p>
        </div>
      </div>
      <div class="grid grid-cols-2 gap-4 justify-end">
        <div>
          <img src="/lonceng.svg">
        </div>
        <a href="/login">
          <img src="/avatar.svg">
        </a>
      </div>
    </div>
    <div class="flex flex-row">
      <div class="sticky top-40 left-0 z-40 w-64 h-full sm:translate-x-0">
        <div class="h-screen py-4 overflow-y-auto bg-white shadow-md rounded-tr-3xl">
          <div class="px-4">
            <a href="/">
              <div class="flex gap-4 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                <img src="beranda0.svg" alt="" class="pl-2">
                <p style="color: rgba(118, 118, 118, 1)">
                  Beranda
                </p>
              </div>
            </a>
            <div class="pt-4">
              <a href="/absensi">
                <div class="flex gap-4 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                  <img src="absen.svg" alt="" class="pl-2">
                  <p style="color: rgba(118, 118, 118, 1)">
                    Absensi
                  </p>
                </div>
              </a>
            </div>
            <div class="pt-4">
              <a href="/meet">
                <div class="flex gap-4 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                  <img src="meet.svg" alt="" class="pl-2">
                  <p style="color: rgba(118, 118, 118, 1)">
                    Meet
                  </p>
                </div>
              </a>
            </div>
            <div class="pt-4">
              <a href="/pengguna">
                <div class="flex gap-2 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                  <img src="pengguna2.svg" alt="" class="pl-2">
                  <p style="color: rgba(0, 117, 255, 1)">
                    Pengguna
                  </p>
                </div>
              </a>
            </div>
            <div class="pt-4">
              <a href="#">
                <div class="flex gap-1 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                  <img src="pengelola.png" alt="" class="">
                  <p style="color: rgba(118, 118, 118, 1)">
                    Pengelola
                  </p>
                </div>
              </a>
            </div>
            <div class="pt-4">
              <a href="#">
                <div class="flex gap-4 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                  <img src="setting.svg" alt="" class="pl-2">
                  <p style="color: rgba(118, 118, 118, 1)">
                    Konfigurasi
                  </p>
                </div>
              </a>
            </div>
            <div class="pt-4">
              <a href="/akun">
                <div class="flex gap-4 hover:bg-blue-100 py-2 hover:rounded-md transition-all">
                  <img src="akun.svg" alt="" class="pl-2">
                  <p style="color:rgba(118, 118, 118, 1)">
                    Akun
                  </p>
                </div>
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class="w-full card md:w-10/12 my-4 lg:my-0 md:mx-4">
        <div class="flex flex-col">
          <div class="bg-white flex flex-col-reverse md:flex-row w-full shadow-lg">
            <div class="flex md:flex-grow flex-col py-6 px-6">
              <div class="text-xl text-neutral-darkness mb-2">
                Tambah Akun
              </div>
              <div class="relative">
                <div for="text" class="mb-4 pl-1 text-gray-600">
                  Nama Depan
                </div>
                <input
                  v-model="inputnamadep"
                  type="text"
                  name="email"
                  placeholder=""
                  class="w-64 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
                >
              </div>
              <div class="relative">
                <div for="text" class="mb-4 pl-1 text-gray-600">
                  Nama Belakang
                </div>
                <input
                  v-model="inputnamabel"
                  type="text"
                  name="email"
                  placeholder=""
                  class="w-64 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
                >
              </div>
              <div class="mt-4">
                <div class="text-neutral-dark">
                  ID
                </div>
                <div class="text-neutral-darkness w-full text-md font-medium mt-2">
                  <input
                    v-model="inputid"
                    type="tell"
                    name="phone"
                    placeholder=""
                    class="w-64 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
                  >
                </div>
              </div>
              <div class="mt-4">
                <div class="text-neutral-dark">
                  Jabatan
                </div>
                <div class="text-neutral-darkness w-full text-medium font-medium mt-2">
                  <input
                    v-model="inputjabatan"
                    type="text"
                    name="fullname"
                    placeholder=""
                    class="w-64 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
                  >
                </div>
              </div>
              <div class="mt-4">
                <div class="text-neutral-dark">
                  Passion
                </div>
                <div class="text-neutral-darkness w-full text-medium font-medium mt-2">
                  <input
                    v-model="inputpass"
                    type="text"
                    name="fullname"
                    placeholder=""
                    class="w-64 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
                  >
                </div>
              </div>
              <div class="mt-4">
                <div class="text-neutral-dark">
                  Gender
                </div>
                <div class="text-neutral-darkness w-full text-medium font-medium mt-2">
                  <input
                    v-model="inputgender"
                    type="text"
                    name="fullname"
                    placeholder=""
                    class="w-64 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
                  >
                </div>
              </div>
              <div class="mt-4">
                <div class="text-neutral-dark">
                  Email
                </div>
                <div class="text-neutral-darkness w-full text-medium font-medium mt-2">
                  <input
                    v-model="inputemail"
                    type="text"
                    name="fullname"
                    placeholder=""
                    class="w-64 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
                  >
                </div>
              </div>
              <div class="mt-4">
                <div class="text-neutral-dark">
                  Password
                </div>
                <div class="text-neutral-darkness w-full text-medium font-medium mt-2">
                  <input
                    v-model="inputpw"
                    type="password"
                    name="fullname"
                    placeholder=""
                    class="w-64 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
                  >
                </div>
              </div>
              <div class="flex justify-end">
                <button class="uppercase hover:opacity-90 w-22 font-semibold bg-blue-700 text-white rounded-md focus:outline-none px-4 py-2" @click="create()">
                  Create
                </button>
              </div>
              <!--Default radio without label-->
              <div class="flex items-center">
                <input
                  id="checked-checkbox"
                  v-model="isactive"
                  checked
                  type="checkbox"
                  value=""
                  class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
                >
                <label for="checked-checkbox" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">Setuju Dan Lanjutkan</label>
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
      inputnamadep: null,
      inputnamabel: null,
      inputid: null,
      inputjabatan: null,
      inputpw: null,
      inputgender: null,
      inputemail: null,
      isactive: false,
      inputpass: null
    }
  },
  methods: {
    toggleShow () {
    },
    async create () {
      try {
        await this.$axios.$post('https://7fcf-2001-448a-5040-6858-95a1-522a-aa10-7a83.ngrok-free.app/api/users',
          {
            first_name: this.inputnamadep,
            last_name: this.inputnamabel,
            id_user: this.inputid,
            job: this.inputjabatan,
            position: this.inputpass,
            gender: this.inputgender,
            email: this.inputemail,
            is_active: this.isactive,
            password: this.inputpw
          },
          {
            headers: { 'ngrok-skip-browser-warning': '123123' }
          }
        ).then((res) => {
          this.$router.replace('/pengguna')
          this.$toast.success('Tambah Akun Berhasil')
          // this.$cookiz.get('user')
          // this.$cookiz.remove('user')
        })
      } catch (error) {
        console.log(error)
      }
    }
  }
}
</script>
