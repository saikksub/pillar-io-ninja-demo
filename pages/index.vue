<template>
  <div>
    <div class="h-[12px] sticky top-0">
      <div class="flex items-center">
        <div class="flex-grow" />
        <button class="p-1 h-12 w-12">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M7.217 10.907a2.25 2.25 0 100 2.186m0-2.186c.18.324.283.696.283 1.093s-.103.77-.283 1.093m0-2.186l9.566-5.314m-9.566 7.5l9.566 5.314m0 0a2.25 2.25 0 103.935 2.186 2.25 2.25 0 00-3.935-2.186zm0-12.814a2.25 2.25 0 103.933-2.185 2.25 2.25 0 00-3.933 2.185z" />
          </svg>
        </button>
      </div>
    </div>
    <div class="relative h-aut mb-4">
      <div class="flex items-center justify-center pt-6">
        <img
          class="h-[98px] w-[98px] rounded-full"
          src="https://res.cloudinary.com/pillario/image/upload/c_thumb,g_custom,w_300,h_300/user-image/page/1a8afd21-5e4c-41e3-a84e-390a2f4fba69?_reload=5b4f3ce0-58c3-11ed-ac12-71127e41ec3b"
        >
      </div>
      <div class="flex items-center justify-center h-auto gap-2 mt-2">
        <p class="text-lg text-white mt-1 text-center">
          {{ profile.username }}
        </p>
        <div class="w-6 h-6 -mb-[4px]">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={1.5} stroke="currentColor" className="w-6 h-6">
            <path strokeLinecap="round" strokeLinejoin="round" d="M9 12.75L11.25 15 15 9.75M21 12c0 1.268-.63 2.39-1.593 3.068a3.745 3.745 0 01-1.043 3.296 3.745 3.745 0 01-3.296 1.043A3.745 3.745 0 0112 21c-1.268 0-2.39-.63-3.068-1.593a3.746 3.746 0 01-3.296-1.043 3.745 3.745 0 01-1.043-3.296A3.745 3.745 0 013 12c0-1.268.63-2.39 1.593-3.068a3.745 3.745 0 011.043-3.296 3.746 3.746 0 013.296-1.043A3.746 3.746 0 0112 3c1.268 0 2.39.63 3.068 1.593a3.746 3.746 0 013.296 1.043 3.746 3.746 0 011.043 3.296A3.745 3.745 0 0121 12z" />
          </svg>
        </div>
      </div>
      <p class="text-center text-sm font-light">
        {{ profile.info }}
      </p>
    </div>
    <div class="relative">
      <ul>
        <li
          v-for="item in socialMediaItems"
          :key="item.id"
          class="gap-2 w-full bg-white rounded-lg text-black h-[64px] mb-6 px-4"
        >
          <div class="flex items-center gap-3 h-full">
            <img class="w-6 h-6" :src="item.iconSrc">
            <div class="flex-grow h-auto text-center">
              {{ item.text }}
            </div>
          </div>
        </li>
      </ul>
    </div>
    <div class="flex items-center justify-center h-auto mt-4 gap-3 py-6">
      <button
        v-for="item in extraLinks"
        :key="item.id"
        class="rounded-full bg-white p-2"
      >
        <img :alt="item.text" :src="item.iconSrc" class="h-6 w-auto">
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      profile: {
        username: 'Ninja',
        verified: true,
        info: 'I love video games 👾'
      },
      socialMediaItems: [
        {
          id: 'link-item-youtube-1',
          text: 'Ninja Gaming',
          iconSrc: '/youtube-icon.svg'
        },
        {
          id: 'link-item-youtube-2',
          text: 'Ninja Vods',
          iconSrc: '/youtube-icon.svg'
        },
        {
          id: 'link-item-youtube-3',
          text: 'Ninja Shorts',
          iconSrc: '/youtube-icon.svg'
        },
        {
          id: 'link-item-gful-3',
          text: 'GFUL',
          iconSrc: '/youtube-icon.svg'
        },
        {
          id: 'link-item-insta-3',
          text: 'Instagram',
          iconSrc: '/instagram.svg'
        },
        {
          id: 'link-item-twitter-3',
          text: 'Twitter',
          iconSrc: '/twitter.svg'
        },
        {
          id: 'link-item-twitch-3',
          text: 'Twitch',
          iconSrc: '/twitch.svg'
        },
        {
          id: 'link-item-merch-3',
          text: 'Merch!',
          iconSrc: '/cart.svg'
        },
        {
          id: 'link-item-text_me-3',
          text: 'Text Me!',
          iconSrc: '/phone.svg'
        },
        {
          id: 'link-item-masterclass-3',
          text: 'Masterclass',
          iconSrc: '/teach.svg'
        }
      ],
      extraLinks: [
        {
          id: 'sl-email',
          src: 'mailto:saikksub@gmail.com',
          iconSrc: '/email.svg'
        },
        {
          id: 'sl-facebook',
          src: 'https://facebook.com',
          iconSrc: '/facebook.svg'
        },
        {
          id: 'sl-instagram',
          src: 'https://instagram.com',
          iconSrc: '/instagram.svg'
        }
      ]
    }
  }
}
</script>
