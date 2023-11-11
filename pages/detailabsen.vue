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
      <div class="flex flex-col w-full">
        <div class="px-8 py-4">
          <div class="bg-white w-full h-full rounded-t-lg shadow-lg">
            <div class="px-12 py-4">
              <div class="relative">
                <h1 class="font-bold text-lg" style="color: rgba(68, 68, 68, 1)">
                  Detail
                </h1>
                <div class="pt-8">
                  <div class="w-80 h-max rounded-lg" style="background-color: rgba(242, 251, 255, 1)">
                    <div class="px-2 py-2">
                      <div class="flex justify-between">
                        <h1 class="font-medium text-base" style="color:rgba(68, 68, 68, 1)">
                          Alvin Top Ahmad
                        </h1>
                        <span class="w-14 h-7 text-center text-white font-semibold text-sm rounded-full" style="background: linear-gradient(90deg, #C4A7F4 0%, #B7B5F4 35.42%, #A8C8F5 63.02%, #95DEF7 100%">
                          <p class="translate-y-1">
                            FE Dev
                          </p>
                        </span>
                      </div>
                      <div class="font-bold text-sm" style="color: rgba(155, 155, 155, 1)">
                        <p>
                          ID:234598
                        </p>
                        <p>
                          alvin@gmail.com
                        </p>
                        <p>
                          098733927
                        </p>
                        <div class="flex justify-end text-base">
                          Magang
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="flex w-full py-8">
                <div class="bg-blue-100 h-full" style="width: 800px">
                  <div class="px-4 py-4 border-b">
                    <div>
                      <h1 class="font-semibold" style="color: rgba(68, 68, 68, 1)">
                        Kehadiran Tahun 2022
                      </h1>
                      <div class="flex justify-between">
                        <p class="font-semibold" style="color: rgba(0, 117, 255, 1)">
                          Percentage 90%
                        </p>
                        <div class="w-28">
                          <v-select :options="['2022','2023','2024']" placeholder="Tahun" />
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="py-4" style="width: 800px">
                    <canvas
                      id="my-chart-id"
                    />
                  </div>
                </div>
                <div class="w-full items-center">
                  <div class="flex justify-center">
                    <div class="flex flex-col">
                      <h1 class="font-bold text-lg" style="color: rgba(68, 68, 68, 1)">
                        Absen Presentace
                      </h1>
                      <div class="pt-2 px-4 translate-y-6">
                        <img src="present.svg">
                      </div>
                      <div class="pt-12">
                        <h1 class="font-bold text-lg" style="color: rgba(68, 68, 68, 1)">
                          Rekap Absen
                        </h1>
                        <div class="w-28">
                          <v-select :options="['2022','2023','2024']" placeholder="Tahun" />
                        </div>
                        <div class="w-28">
                          <v-select :options="['2022','2023','2024']" placeholder="Tahun" />
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="px-8 py-4">
          <div class="bg-white w-full h-full rounded-t-lg shadow-lg">
            <div class="px-12 py-4">
              <div>
                <h1 class="font-semibold text-lg pt-8" style="color: rgba(68, 68, 68, 1)">
                  Absensi
                </h1>
                <div class="pt-8">
                  <table class="items-center w-full border">
                    <thead>
                      <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(0, 117, 255, 1)">
                        <th class="py-4 px-4">
                          Date
                        </th>
                        <th class="py-4 px-4">
                          Lokasi
                        </th>
                        <th class="py-4 px-4">
                          Checkin
                        </th>
                        <th class="py-4 px-4">
                          Yang di Kerjakan
                        </th>
                        <th class="py-4 px-4">
                          Chec out
                        </th>
                        <th class="py-4 px-4">
                          Yang di Kerjakan
                        </th>
                        <th class="py-4 px-4">
                          Hasil
                        </th>
                        <th class="py-4 px-4">
                          Kehadiran
                        </th>
                      </tr>
                    </thead>
                    <tbody>
                      <tr v-for="(absen, index) in detail" :key="index" class="border-b py-4">
                        <td class=" text-sm items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                          {{ absen.presence__users.presence.date_presence }}
                        </td>
                        <td class="text-sm items-center py-4 text-center font-semibold" style="color: rgba(126, 126, 126, 1)">
                          {{ absen.longitude }}
                        </td>
                        <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                          {{ absen.type }}
                        </td>
                        <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                          {{ absen.latitude }}
                        </td>
                        <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                          {{ absen.type }}
                        </td>
                        <td class="text-sm items-center py-4 text-center" style="color: rgba(126, 126, 126, 1)">
                          {{ absen.finished_task }}
                        </td>
                        <td class="items-center py-4 text-center text-sm">
                          <div>
                            <a href="/detailabsen">
                              <p class="font-semibold underline underline-offset-1" style="color: rgba(0, 117, 255, 1)">
                                Lihat Foto
                              </p>
                            </a>
                          </div>
                        </td>
                        <td class="items-center py-2 text-center text-sm">
                          <div class="w-max h-9 px-2 rounded-lg mx-auto" style="background-color: rgba(206, 255, 211, 1)">
                            <p class="text-center py-2 font-semibold text-sm" style="color: rgba(0, 255, 25, 1)">
                              {{ absen.description }}
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
  </div>
</template>
<script>
import Chart from 'chart.js/auto'

export default {
  name: 'BarChart',
  data () {
    return {
      selected: null,
      minimize: null,
      detail: null,
      chartData: {
        type: 'bar',
        data: {
          labels: ['Jan', 'Feb', 'Mar', 'apr', 'mei', 'jun', 'jul', 'Ags', 'Sep', 'otk', 'Nov', 'Des'],
          datasets: [{
            label: 'Tabel Hadir',
            data: [85, 98, 100, 83, 85, 95, 100, 100, 82, 88, 100, 76],
            backgroundColor: [
              'rgba(0, 117, 255, 1)'
            ]
          }]
        }
      }
    }
  },
  mounted () {
    this.renderChart()
    this.getData()
  },
  methods: {
    renderChart () {
      window.myChart = new Chart(document.getElementById('my-chart-id'), this.chartData)
    },
    async getData () {
      try {
        await this.$axios.$get('https://7fcf-2001-448a-5040-6858-95a1-522a-aa10-7a83.ngrok-free.app/api/userdetail', {
          params: {
            nama: this.cari
          },
          headers: { 'ngrok-skip-browser-warning': '123123' }
        })
          .then((res) => {
            this.detail = res.message
          })
      } catch (error) {
        alert(alert.response.data.message)
      }
    }
  }
}
</script>
