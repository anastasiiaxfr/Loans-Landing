<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<script setup lang="ts">
useSeoMeta({
  title: "★Loans | Xforeal★",
  ogTitle: "My Amazing Nuxt + Sass Site",
  description: "This is my amazing site, let me tell you all about it.",
  ogDescription: "This is my amazing site, let me tell you all about it.",
  ogImage: "fav/og.jpg",
  twitterCard: "summary_large_image",
});

useHead({
  link: [
    { rel: "shortcut icon", href: "fav/favicon.ico", type: "image/x-icon" },
    { rel: "icon", href: "fav/favicon.ico", type: "image/x-icon" },
    { rel: "icon", href: "fav/favicon.png", type: "image/x-icon" },
    { rel: "apple-touch-icon", href: "fav/apple-touch-icon.png", sizes: "180x180" },
    { rel: "icon", type: "image/png", href: "fav/favicon-96x96.png", sizes: "96x96" },
    { rel: "mask-icon", href: "fav/safari-pinned-tab.svg", color: "#2a6877" },
    { rel: "manifest", href: "fav/site.webmanifest" },
  ],
  meta: [
    { name: "msapplication-TileColor", content: "#2a6877" },
    { name: "theme-color", content: "#2a6877" },
  ],
  script: [
    {
      async: true,
      type: "application/ld+json",
      children: JSON.stringify({
        "@context": "http://schema.org/",
        "@type": "Organization",
        name: "XFR",
        brand: "XFR",
        alternateName: "XFR",
        url: "https://loans-xfr.netlify.app/",
        logo: "https://loans-xfr.netlify.app/images/logo.svg",
        address: {
          "@type": "PostalAddress",
          streetAddress: "xxx",
          addressLocality: "Київ",
          addressCountry: "Україна",
        },
        contactPoint: [
          {
            "@type": "ContactPoint",
            telephone: "380630633226",
            email: "office@xfr-investments.com",
            contactType: "customer support",
            areaServed: "UA",
            availableLanguage: ["Ukrain"],
          },
        ],
        sameAs: [
          "https://www.facebook.com/",
          "https://www.instagram.com/",
          "https://www.tiktok.com/",
          "https://twitter.com/",
          "https://www.youtube.com/channel/",
          "https://t.me/XFR_club",
        ],
      }),
    },
  ],
});
</script>
