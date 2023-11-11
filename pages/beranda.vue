<template>
  <div>
    <navbar1 />
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
                    <img src="beranda.svg" alt="" class="pl-2 w-6">
                  </div>
                  <p v-if="!minimize" style="color: rgba(0, 117, 255, 1)">
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
        <div class="grid grid-cols-3 gap-4 px-12">
          <div class="bg-white w-80 h-24 shadow-lg rounded-lg">
            <div class="px-2 py-2">
              <h1 class="font-semibold text-base" style="color: rgba(68, 68, 68, 1)">
                Total Magang
              </h1>
              <div class="flex justify-between">
                <p class="pt-4 font-semibold text-lg" style="color: rgba(0, 117, 255, 1)">
                  10
                </p>
                <div>
                  <img src="magang.svg" alt="">
                </div>
              </div>
            </div>
          </div>
          <div class="bg-white w-80 h-24 shadow-lg rounded-lg">
            <div class="px-2 py-2">
              <h1 class="font-semibold text-base" style="color: rgba(68, 68, 68, 1)">
                Total Admin
              </h1>
              <div class="flex justify-between">
                <p class="pt-4 font-semibold text-lg" style="color: rgba(0, 117, 255, 1)">
                  3
                </p>
                <div>
                  <img src="admin.svg" alt="">
                </div>
              </div>
            </div>
          </div>
          <div class="bg-white w-80 h-24 shadow-lg rounded-lg">
            <div class="px-2 py-2">
              <h1 class="font-semibold text-base" style="color: rgba(68, 68, 68, 1)">
                Total Pengguna
              </h1>
              <div class="flex justify-between">
                <p class="pt-4 font-semibold text-lg" style="color: rgba(0, 117, 255, 1)">
                  11
                </p>
                <div>
                  <img src="pg.svg" alt="">
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="px-8 py-4">
          <div class="bg-white w-full h-full rounded-t-lg shadow-lg">
            <div class="px-12 py-4">
              <div style="background-color: rgba(244, 251, 255, 1)">
                <div class="px-4 py-4 border-b">
                  <div>
                    <h1 class="font-semibold" style="color: rgba(68, 68, 68, 1)">
                      Kehadiran Tahun 2022
                    </h1>
                    <div class="flex justify-between">
                      <p class="font-semibold" style="color: rgba(0, 117, 255, 1)">
                        Percentage 90%
                      </p>
                      <div class="grid grid-cols-2 gap-4">
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
                <div class="py-4" style="width: 800px">
                  <canvas
                    id="my-chart-id"
                  />
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
                  Konfigurasi
                </h1>
                <div class="pt-8">
                  <table class="items-center w-full border">
                    <thead>
                      <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(0, 117, 255, 1)">
                        <th class="py-4">
                          No
                        </th>
                        <th>Keterangan Libur</th>
                        <th>Tanggal</th>
                        <th>Action</th>
                      </tr>
                    </thead>
                    <tbody>
                      <tr class="border-b py-4">
                        <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                          1
                        </td>
                        <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                          Liburan Hari Nyepi
                        </td>
                        <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                          29/3/2023
                        </td>
                        <td class="flex gap-2 py-4 justify-center">
                          <img src="sampah.svg">
                          <img src="pensil.svg">
                        </td>
                      </tr>
                      <tr class="border-b py-4">
                        <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                          2
                        </td>
                        <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                          Liburan Hari Nyepi
                        </td>
                        <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                          29/3/2023
                        </td>
                        <td class="flex gap-2 py-4 justify-center">
                          <img src="sampah.svg">
                          <img src="pensil.svg">
                        </td>
                      </tr>
                      <tr class="border-b py-4">
                        <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                          3
                        </td>
                        <td class="items-center py-4 text-center font-semibold" style="color: rgba(68, 68, 68, 1)">
                          Liburan Hari Nyepi
                        </td>
                        <td class="items-center py-4 text-center text-sm" style="color: rgba(126, 126, 126, 1)">
                          29/3/2023
                        </td>
                        <td class="flex gap-2 py-4 justify-center">
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
    </div>
  </div>
</template>

<script>
import Chart from 'chart.js/auto'

export default {
  name: 'BarChart',
  data () {
    return {
      minimize: false,
      selected: null,
      chartData: {
        type: 'bar',
        data: {
          labels: [],
          // labels: ['Jan', 'Feb', 'Mar', 'apr', 'mei', 'jun', 'jul', 'Ags', 'Sep', 'otk', 'Nov', 'Des'],
          datasets: [{
            label: 'Tabel Hadir',
            data: [],
            backgroundColor: [
              'rgba(0, 117, 255, 1)'
            ]
          }]
        }
      }
    }
  },
  mounted () {
    // this.renderChart()
    this.getData()
  },
  methods: {
    renderChart () {
      window.myChart = new Chart(document.getElementById('my-chart-id'), this.chartData)
    },
    async getData () {
      try {
        await this.$axios.$get('https://7fcf-2001-448a-5040-6858-95a1-522a-aa10-7a83.ngrok-free.app/api/beranda', {
          headers: { 'ngrok-skip-browser-warning': '123123' }
        })
          .then((res) => {
            // this.Chart = res.message
            this.chartData.data.labels = Object.keys(res.message)
            Object.values(res.message).forEach((e) => {
              this.chartData.data.datasets[0].data.push(e.length)
            })
            // this.chartData.data.datasets[0].data = Object.values(res.message).length
            this.renderChart()
          })
      } catch (error) {
        alert(alert.response.data.message)
      }
    }
  }
}
</script>
