<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <MegaMenuVue :title="'منو'" :list="list" :array="'jobs'" @showItem="showItem" @showCategory="showCategory"></MegaMenuVue>
    </div>
    <router-view/>
  </div>
</template>

<script>
import MegaMenuVue from '@/components/megaMenu.vue'

export default {
  name: 'Home',
  components: {
    MegaMenuVue
  },
  data () {
    return {
      list: [
        {
          id: 11,
          title: 'توسعه فردی',
          jobs: [
            {
              id: 80,
              created_at: '2023-02-23T12:42:09.873917+03:30',
              modified_at: '2023-04-06T14:11:40.325726+04:30',
              is_deleted: false,
              name: 'توسعه فردی',
              title: 'توسعه فردی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 11
            },
            {
              id: 76,
              created_at: '2023-02-12T12:24:18.846848+03:30',
              modified_at: '2023-04-06T16:25:43.837960+04:30',
              is_deleted: false,
              name: 'مهارت های نرم',
              title: 'مهارت های نرم',
              description: '',
              created_by: null,
              modified_by: null,
              category: 11
            }
          ]
        },
        {
          id: 13,
          title: 'توسعه و منابع انسانی',
          jobs: [
            {
              id: 57,
              created_at: '2023-02-11T11:43:47.496190+03:30',
              modified_at: '2023-04-06T14:10:18.487686+04:30',
              is_deleted: false,
              name: 'آموزش',
              title: 'آموزش',
              description: '',
              created_by: null,
              modified_by: null,
              category: 13
            },
            {
              id: 87,
              created_at: '2023-03-06T18:50:24.622444+03:30',
              modified_at: '2023-04-06T16:25:26.919857+04:30',
              is_deleted: false,
              name: 'مسیر شغلی',
              title: 'مسیر شغلی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 13
            },
            {
              id: 59,
              created_at: '2023-02-11T11:44:13.955661+03:30',
              modified_at: '2023-04-06T16:25:37.780179+04:30',
              is_deleted: false,
              name: 'منابع انسانی',
              title: 'منابع انسانی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 13
            }
          ]
        },
        {
          id: 6,
          title: 'سایر',
          jobs: []
        },
        {
          id: 5,
          title: 'فروش و بازاریابی',
          jobs: [
            {
              id: 23,
              created_at: '2023-02-11T11:17:18.571004+03:30',
              modified_at: '2023-02-11T11:17:18.571051+03:30',
              is_deleted: false,
              name: 'بازاریابی',
              title: 'بازاریابی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 5
            },
            {
              id: 43,
              created_at: '2023-02-11T11:37:17.678609+03:30',
              modified_at: '2023-02-11T11:37:17.678653+03:30',
              is_deleted: false,
              name: 'تولید محتوا',
              title: 'تولید محتوا',
              description: '',
              created_by: null,
              modified_by: null,
              category: 5
            },
            {
              id: 44,
              created_at: '2023-02-11T11:37:27.479468+03:30',
              modified_at: '2023-02-11T11:37:27.479517+03:30',
              is_deleted: false,
              name: 'دیجیتال مارکتینگ',
              title: 'دیجیتال مارکتینگ',
              description: '',
              created_by: null,
              modified_by: null,
              category: 5
            },
            {
              id: 61,
              created_at: '2023-02-11T11:44:44.703477+03:30',
              modified_at: '2023-04-06T15:59:44.500672+04:30',
              is_deleted: false,
              name: 'روابط عمومی',
              title: 'روابط عمومی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 5
            },
            {
              id: 45,
              created_at: '2023-02-11T11:37:49.224737+03:30',
              modified_at: '2023-04-06T16:00:00.087541+04:30',
              is_deleted: false,
              name: 'سئو',
              title: 'سئو',
              description: '',
              created_by: null,
              modified_by: null,
              category: 5
            },
            {
              id: 56,
              created_at: '2023-02-11T11:43:02.767026+03:30',
              modified_at: '2023-04-06T16:00:14.472299+04:30',
              is_deleted: false,
              name: 'شبکه های اجتماعی',
              title: 'شبکه های اجتماعی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 5
            },
            {
              id: 22,
              created_at: '2023-02-11T11:17:06.823701+03:30',
              modified_at: '2023-02-11T11:17:06.823750+03:30',
              is_deleted: false,
              name: 'فروش',
              title: 'فروش',
              description: '',
              created_by: null,
              modified_by: null,
              category: 5
            },
            {
              id: 46,
              created_at: '2023-02-11T11:38:14.362361+03:30',
              modified_at: '2023-04-06T16:26:51.853673+04:30',
              is_deleted: false,
              name: 'پشتیبانی و امور مشتری',
              title: 'پشتیبانی و امور مشتری',
              description: '',
              created_by: null,
              modified_by: null,
              category: 5
            }
          ]
        },
        {
          id: 2,
          title: 'فناوری اطلاعات IT',
          jobs: [
            {
              id: 26,
              created_at: '2023-02-11T11:18:45.144204+03:30',
              modified_at: '2023-04-06T14:10:04.610849+04:30',
              is_deleted: false,
              name: 'DevOps',
              title: 'DevOps',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 66,
              created_at: '2023-02-11T11:46:54.105747+03:30',
              modified_at: '2023-04-06T14:10:12.097004+04:30',
              is_deleted: false,
              name: 'Docker',
              title: 'Docker',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 7,
              created_at: '2023-02-11T11:11:10.497844+03:30',
              modified_at: '2023-02-11T11:11:10.497912+03:30',
              is_deleted: false,
              name: 'برنامه نویس #C',
              title: 'برنامه نویس #C',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 10,
              created_at: '2023-02-11T11:12:22.113429+03:30',
              modified_at: '2023-02-11T11:12:22.113460+03:30',
              is_deleted: false,
              name: 'برنامه نویس ++C',
              title: 'برنامه نویس ++C',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 12,
              created_at: '2023-02-11T11:13:04.949747+03:30',
              modified_at: '2023-02-11T11:13:04.949795+03:30',
              is_deleted: false,
              name: 'برنامه نویس Angular',
              title: 'برنامه نویس Angular',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 13,
              created_at: '2023-02-11T11:13:35.862345+03:30',
              modified_at: '2023-02-11T11:13:35.862401+03:30',
              is_deleted: false,
              name: 'برنامه نویس Django',
              title: 'برنامه نویس Django',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 11,
              created_at: '2023-02-11T11:12:42.229252+03:30',
              modified_at: '2023-02-11T11:12:42.229281+03:30',
              is_deleted: false,
              name: 'برنامه نویس Java',
              title: 'برنامه نویس Java',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 18,
              created_at: '2023-02-11T11:15:28.075755+03:30',
              modified_at: '2023-02-11T11:15:28.075799+03:30',
              is_deleted: false,
              name: 'برنامه نویس JavaScript',
              title: 'برنامه نویس JavaScript',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 14,
              created_at: '2023-02-11T11:13:46.251033+03:30',
              modified_at: '2023-02-11T11:13:46.251069+03:30',
              is_deleted: false,
              name: 'برنامه نویس Laravel',
              title: 'برنامه نویس Laravel',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 15,
              created_at: '2023-02-11T11:14:00.087514+03:30',
              modified_at: '2023-02-11T11:14:00.087561+03:30',
              is_deleted: false,
              name: 'برنامه نویس Net.',
              title: 'برنامه نویس Net.',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 16,
              created_at: '2023-02-11T11:14:18.948314+03:30',
              modified_at: '2023-02-11T11:14:18.948352+03:30',
              is_deleted: false,
              name: 'برنامه نویس Node.JS',
              title: 'برنامه نویس Node.JS',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 40,
              created_at: '2023-02-11T11:34:55.689772+03:30',
              modified_at: '2023-02-11T11:34:55.689820+03:30',
              is_deleted: false,
              name: 'برنامه نویس PHP',
              title: 'برنامه نویس PHP',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 2,
              created_at: '2023-02-11T10:05:09.576370+03:30',
              modified_at: '2023-02-11T10:05:09.576400+03:30',
              is_deleted: false,
              name: 'برنامه نویس Python',
              title: 'برنامه نویس Python',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 17,
              created_at: '2023-02-11T11:14:41.419824+03:30',
              modified_at: '2023-02-11T11:14:41.419868+03:30',
              is_deleted: false,
              name: 'برنامه نویس React',
              title: 'برنامه نویس React',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 41,
              created_at: '2023-02-11T11:35:31.207050+03:30',
              modified_at: '2023-02-11T11:35:31.207100+03:30',
              is_deleted: false,
              name: 'برنامه نویس Vue.Js',
              title: 'برنامه نویس Vue.Js',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 3,
              created_at: '2023-02-11T10:05:25.256847+03:30',
              modified_at: '2023-02-11T10:05:25.256890+03:30',
              is_deleted: false,
              name: 'برنامه نویس ios',
              title: 'برنامه نویس ios',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 53,
              created_at: '2023-02-11T11:42:24.744527+03:30',
              modified_at: '2023-02-11T11:42:24.744564+03:30',
              is_deleted: false,
              name: 'برنامه نویس اندروید',
              title: 'برنامه نویس اندروید',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 67,
              created_at: '2023-02-11T11:47:55.056896+03:30',
              modified_at: '2023-02-11T11:47:55.056928+03:30',
              is_deleted: false,
              name: 'برنامه نویس بلاک چین',
              title: 'برنامه نویس بلاک چین',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 84,
              created_at: '2023-03-02T17:08:11.954582+03:30',
              modified_at: '2023-04-06T14:11:07.090491+04:30',
              is_deleted: false,
              name: 'تحلیل داده',
              title: 'تحلیل داده',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 8,
              created_at: '2023-02-11T11:11:33.679372+03:30',
              modified_at: '2023-02-11T11:11:33.679403+03:30',
              is_deleted: false,
              name: 'تحلیلگر نرم افزار',
              title: 'تحلیلگر نرم افزار',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 42,
              created_at: '2023-02-11T11:36:39.349450+03:30',
              modified_at: '2023-02-11T11:53:25.875344+03:30',
              is_deleted: false,
              name: 'دانشمند داده',
              title: 'دانشمند داده',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 27,
              created_at: '2023-02-11T11:30:48.767281+03:30',
              modified_at: '2023-04-06T16:00:05.211042+04:30',
              is_deleted: false,
              name: 'شبکه',
              title: 'شبکه',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 21,
              created_at: '2023-02-11T11:16:34.981499+03:30',
              modified_at: '2023-04-06T16:01:23.878300+04:30',
              is_deleted: false,
              name: 'ماشین لرنینگ',
              title: 'ماشین لرنینگ',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 79,
              created_at: '2023-02-23T11:29:42.135596+03:30',
              modified_at: '2023-04-06T16:01:39.960315+04:30',
              is_deleted: false,
              name: 'مدیریت داده',
              title: 'مدیریت داده',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 89,
              created_at: '2023-03-13T09:52:11.465058+03:30',
              modified_at: '2023-03-13T09:52:11.465086+03:30',
              is_deleted: false,
              name: 'معماری نرم افزار',
              title: 'معماری نرم افزار',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 82,
              created_at: '2023-02-25T10:27:11.943931+03:30',
              modified_at: '2023-02-25T10:27:11.943959+03:30',
              is_deleted: false,
              name: 'مهندس تست نرم افزار',
              title: 'مهندس تست نرم افزار',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 63,
              created_at: '2023-02-11T11:45:16.230741+03:30',
              modified_at: '2023-02-11T11:45:16.230774+03:30',
              is_deleted: false,
              name: 'وردپرس',
              title: 'وردپرس',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            },
            {
              id: 68,
              created_at: '2023-02-11T11:48:18.748218+03:30',
              modified_at: '2023-04-06T16:26:22.389580+04:30',
              is_deleted: false,
              name: 'پایگاه داده',
              title: 'پایگاه داده',
              description: '',
              created_by: null,
              modified_by: null,
              category: 2
            }
          ]
        },
        {
          id: 8,
          title: 'مالی و سرمایه گذاری',
          jobs: [
            {
              id: 52,
              created_at: '2023-02-11T11:41:28.901596+03:30',
              modified_at: '2023-02-11T11:41:28.901626+03:30',
              is_deleted: false,
              name: 'ارز دیجیتال',
              title: 'ارز دیجیتال',
              description: '',
              created_by: null,
              modified_by: null,
              category: 8
            },
            {
              id: 70,
              created_at: '2023-02-11T11:49:09.284539+03:30',
              modified_at: '2023-02-11T11:49:09.284587+03:30',
              is_deleted: false,
              name: 'تحلیل بورس',
              title: 'تحلیل بورس',
              description: '',
              created_by: null,
              modified_by: null,
              category: 8
            },
            {
              id: 49,
              created_at: '2023-02-11T11:40:05.500391+03:30',
              modified_at: '2023-02-11T11:40:05.500436+03:30',
              is_deleted: false,
              name: 'حسابدار',
              title: 'حسابدار',
              description: '',
              created_by: null,
              modified_by: null,
              category: 8
            },
            {
              id: 50,
              created_at: '2023-02-11T11:40:16.410459+03:30',
              modified_at: '2023-02-11T11:40:16.410505+03:30',
              is_deleted: false,
              name: 'فارکس',
              title: 'فارکس',
              description: '',
              created_by: null,
              modified_by: null,
              category: 8
            },
            {
              id: 51,
              created_at: '2023-02-11T11:41:16.245668+03:30',
              modified_at: '2023-02-11T11:41:16.245700+03:30',
              is_deleted: false,
              name: 'مالی',
              title: 'مالی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 8
            }
          ]
        },
        {
          id: 3,
          title: 'محصول',
          jobs: [
            {
              id: 9,
              created_at: '2023-02-11T11:11:49.565861+03:30',
              modified_at: '2023-02-11T11:11:49.565909+03:30',
              is_deleted: false,
              name: 'طراح رابط کاربری UI/UX',
              title: 'طراح رابط کاربری UI/UX',
              description: '',
              created_by: null,
              modified_by: null,
              category: 3
            },
            {
              id: 83,
              created_at: '2023-02-26T11:12:57.392037+03:30',
              modified_at: '2023-02-26T11:13:17.498017+03:30',
              is_deleted: false,
              name: 'طراحی محصول',
              title: 'طراحی محصول',
              description: '',
              created_by: null,
              modified_by: null,
              category: 3
            },
            {
              id: 6,
              created_at: '2023-02-11T11:04:59.621061+03:30',
              modified_at: '2023-04-06T16:01:10.509903+04:30',
              is_deleted: false,
              name: 'مدیر محصول',
              title: 'مدیر محصول',
              description: '',
              created_by: null,
              modified_by: null,
              category: 3
            }
          ]
        },
        {
          id: 10,
          title: 'مدیریت و کسب وکار',
          jobs: [
            {
              id: 73,
              created_at: '2023-02-11T11:54:50.175516+03:30',
              modified_at: '2023-02-14T21:37:49.783617+03:30',
              is_deleted: false,
              name: 'استراتژی',
              title: 'استراتژی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 10
            },
            {
              id: 54,
              created_at: '2023-02-11T11:42:41.884469+03:30',
              modified_at: '2023-02-11T11:55:34.897139+03:30',
              is_deleted: false,
              name: 'بازرگانی',
              title: 'بازرگانی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 10
            },
            {
              id: 75,
              created_at: '2023-02-11T11:56:53.300586+03:30',
              modified_at: '2023-02-11T11:56:53.300616+03:30',
              is_deleted: false,
              name: 'تحلیل کسب و کار',
              title: 'تحلیل کسب و کار',
              description: '',
              created_by: null,
              modified_by: null,
              category: 10
            },
            {
              id: 74,
              created_at: '2023-02-11T11:55:28.581344+03:30',
              modified_at: '2023-02-11T11:55:28.581385+03:30',
              is_deleted: false,
              name: 'مدیریت عملیات',
              title: 'مدیریت عملیات',
              description: '',
              created_by: null,
              modified_by: null,
              category: 10
            },
            {
              id: 77,
              created_at: '2023-02-21T19:16:16.104678+03:30',
              modified_at: '2023-02-21T19:16:16.104724+03:30',
              is_deleted: false,
              name: 'کار آفرینی',
              title: 'کار آفرینی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 10
            },
            {
              id: 88,
              created_at: '2023-03-12T17:35:31.289049+03:30',
              modified_at: '2023-03-12T17:35:31.289075+03:30',
              is_deleted: false,
              name: 'کارآفرینی اجتماعی',
              title: 'کارآفرینی اجتماعی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 10
            },
            {
              id: 81,
              created_at: '2023-02-23T13:24:37.123952+03:30',
              modified_at: '2023-02-23T13:24:37.123982+03:30',
              is_deleted: false,
              name: 'کسب و کار',
              title: 'کسب و کار',
              description: '',
              created_by: null,
              modified_by: null,
              category: 10
            },
            {
              id: 85,
              created_at: '2023-03-03T18:19:32.233927+03:30',
              modified_at: '2023-03-06T18:50:05.279318+03:30',
              is_deleted: false,
              name: 'فینتک',
              title: 'کسب و کار های فینتک',
              description: '',
              created_by: null,
              modified_by: null,
              category: 10
            },
            {
              id: 47,
              created_at: '2023-02-11T11:38:36.680214+03:30',
              modified_at: '2023-04-06T16:27:55.079904+04:30',
              is_deleted: false,
              name: 'کنترل پروژه',
              title: 'کنترل پروژه',
              description: '',
              created_by: null,
              modified_by: null,
              category: 10
            }
          ]
        },
        {
          id: 4,
          title: 'مهندسی',
          jobs: [
            {
              id: 90,
              created_at: '2023-03-28T01:01:19.273465+04:30',
              modified_at: '2023-03-28T01:01:19.273506+04:30',
              is_deleted: false,
              name: 'مهندس نفت',
              title: 'مهندس نفت',
              description: '',
              created_by: null,
              modified_by: null,
              category: 4
            },
            {
              id: 29,
              created_at: '2023-02-11T11:31:15.180929+03:30',
              modified_at: '2023-02-11T11:31:15.180976+03:30',
              is_deleted: false,
              name: 'مهندسی برق',
              title: 'مهندسی برق',
              description: '',
              created_by: null,
              modified_by: null,
              category: 4
            },
            {
              id: 31,
              created_at: '2023-02-11T11:31:42.428283+03:30',
              modified_at: '2023-02-11T11:31:42.428318+03:30',
              is_deleted: false,
              name: 'مهندسی شیمی',
              title: 'مهندسی شیمی',
              description: '',
              created_by: null,
              modified_by: null,
              category: 4
            },
            {
              id: 28,
              created_at: '2023-02-11T11:31:05.369361+03:30',
              modified_at: '2023-02-11T11:31:05.369403+03:30',
              is_deleted: false,
              name: 'مهندسی صنایع',
              title: 'مهندسی صنایع',
              description: '',
              created_by: null,
              modified_by: null,
              category: 4
            },
            {
              id: 33,
              created_at: '2023-02-11T11:32:09.817201+03:30',
              modified_at: '2023-02-11T11:32:09.817233+03:30',
              is_deleted: false,
              name: 'مهندسی عمران',
              title: 'مهندسی عمران',
              description: '',
              created_by: null,
              modified_by: null,
              category: 4
            },
            {
              id: 34,
              created_at: '2023-02-11T11:32:24.985036+03:30',
              modified_at: '2023-02-11T11:32:24.985072+03:30',
              is_deleted: false,
              name: 'مهندسی معماری',
              title: 'مهندسی معماری',
              description: '',
              created_by: null,
              modified_by: null,
              category: 4
            },
            {
              id: 32,
              created_at: '2023-02-11T11:31:54.381852+03:30',
              modified_at: '2023-02-11T11:31:54.381904+03:30',
              is_deleted: false,
              name: 'مهندسی کامپیوتر',
              title: 'مهندسی کامپیوتر',
              description: '',
              created_by: null,
              modified_by: null,
              category: 4
            }
          ]
        },
        {
          id: 12,
          title: 'هنر',
          jobs: [
            {
              id: 62,
              created_at: '2023-02-11T11:45:07.759469+03:30',
              modified_at: '2023-04-06T14:11:51.955300+04:30',
              is_deleted: false,
              name: 'تدوینگر',
              title: 'تدوینگر',
              description: '',
              created_by: null,
              modified_by: null,
              category: 12
            },
            {
              id: 48,
              created_at: '2023-02-11T11:39:09.864101+03:30',
              modified_at: '2023-04-06T16:26:13.465858+04:30',
              is_deleted: false,
              name: 'موشن گرافیست',
              title: 'موشن گرافیست',
              description: '',
              created_by: null,
              modified_by: null,
              category: 12
            },
            {
              id: 4,
              created_at: '2023-02-11T10:05:58.792497+03:30',
              modified_at: '2023-04-06T16:28:01.518774+04:30',
              is_deleted: false,
              name: 'گرافیست',
              title: 'گرافیست',
              description: '',
              created_by: null,
              modified_by: null,
              category: 12
            }
          ]
        },
        {
          id: 9,
          title: 'هوش مصنوعی',
          jobs: [
            {
              id: 20,
              created_at: '2023-02-11T11:16:10.427148+03:30',
              modified_at: '2023-02-11T11:52:46.115226+03:30',
              is_deleted: false,
              name: 'پردازش تصویر',
              title: 'پردازش تصویر',
              description: '',
              created_by: null,
              modified_by: null,
              category: 9
            }
          ]
        }
      ]
    }
  },
  methods: {
    showItem (data) {
      console.log('showItem: ', data)
    },
    showCategory (data) {
      console.log('showCategory: ', data)
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  display: flex;
  justify-content: center;
  gap: 8px;
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
