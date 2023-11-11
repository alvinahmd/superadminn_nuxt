<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <div class="flex px-8 py-4">
      <div>
        <img src="logo.svg" alt="">
      </div>
      <div class="items-center mx-auto pt-4">
        <div class="bg-white px-8 py-2 rounded-full shadow-lg text-center items-center">
          <p class="font-semibold">
            Hii,
            <span style="color: rgba(0, 117, 255, 1)"> {{ $nuxt.$cookiz.get('auth').user.first_name }}</span>
          </p>
        </div>
      </div>
      <div class="grid grid-cols-2 gap-4 justify-end">
        <div>
          <a href="/notif">
            <img src="lonceng.svg" alt="">
          </a>
        </div>
        <div>
          <img src="profil.svg" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// export default {
//   data () {
//     return {
//       password: null,
//       inputid: null,
//       inputPass: null
//     }
//   },
//   methods: {
//     toggleShow () {
//     },
//     async login () {
//       try {
//         await this.$axios.$post('https://818d-2001-448a-5040-7137-b178-e892-e979-278c.ngrok-free.app/api/login',
//           {
//             headers: { 'ngrok-skip-browser-warning': '123123' },
//             id_user: this.inputid,
//             password: this.inputPass
//           }).then((res) => {
//           this.$nuxt.$cookiz.set('auth', res)
//           this.$router.replace('/beranda')
//           this.$toast.success(' Login berhasil')
//           // this.$cookiz.get('user')
//           // this.$cookiz.remove('user')
//         })
//       } catch (error) {
//         console.log(error)
//       }
//     }
//   }
// }
</script>
