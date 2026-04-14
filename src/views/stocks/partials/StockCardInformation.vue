<script setup lang="ts">
import { Card, CardContent, CardHeader, CardTitle } from '@/components/ui/card'
</script>

<template>
  <Card>
    <CardHeader class="-mb-4">
      <CardTitle class="text-3xl">Information</CardTitle>
    </CardHeader>
    <hr />
    <CardContent class="space-y-8">
      <img src="/src/assets/img/aapl.png" alt="aapl" class="h-16 rounded-2xl" />
      <div class="flex items-center justify-around">
        <div class="flex flex-col gap-4">
          <div class="flex items-center gap-2">
            <span class="font-bold">Website :</span>
            <a
              href="https://www.apple.com"
              target="_blank"
              rel="noopener noreferrer"
              class="hover:underline"
            >
              https://www.apple.com
            </a>
          </div>
          <div class="flex items-center gap-2">
            <span class="font-bold">Country :</span>
            <span>US</span>
          </div>
        </div>

        <div class="flex flex-col gap-4">
          <div class="flex items-center gap-2">
            <span class="font-bold">Sector :</span>
            <span>Technology</span>
          </div>
          <div class="flex items-center gap-2">
            <span class="font-bold">Industry :</span>
            <span>Consumer Electronics</span>
          </div>
        </div>
      </div>

      <div>
        <div class="font-bold">Description :</div>
        <div class="mt-2 max-h-40 overflow-y-auto rounded border p-4">
          Apple Inc. designs, manufactures, and markets smartphones, personal computers, tablets,
          wearables, and accessories worldwide. The company offers iPhone, a line of smartphones;
          Mac, a line of personal computers; iPad, a line of multi-purpose tablets; and wearables,
          home, and accessories comprising AirPods, Apple TV, Apple Watch, Beats products, and
          HomePod. It also provides AppleCare support and cloud services; and operates various
          platforms, including the App Store that allow customers to discover and download
          applications and digital content, such as books, music, video, games, and podcasts, as
          well as advertising services include third-party licensing arrangements and its own
          advertising platforms. In addition, the company offers various subscription-based
          services, such as Apple Arcade, a game subscription service; Apple Fitness+, a
          personalized fitness service; Apple Music, which offers users a curated listening
          experience with on-demand radio stations; Apple News+, a subscription news and magazine
          service; Apple TV+, which offers exclusive original content; Apple Card, a co-branded
          credit card; and Apple Pay, a cashless payment service, as well as licenses its
          intellectual property. The company serves consumers, and small and mid-sized businesses;
          and the education, enterprise, and government markets. It distributes third-party
          applications for its products through the App Store. The company also sells its products
          through its retail and online stores, and direct sales force; and third-party cellular
          network carriers, wholesalers, retailers, and resellers. Apple Inc. was founded in 1976
          and is headquartered in Cupertino, California.
        </div>
      </div>
    </CardContent>
  </Card>
</template>
