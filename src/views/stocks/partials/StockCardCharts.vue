<script setup lang="ts">
import { Card, CardContent, CardHeader, CardTitle } from '@/components/ui/card'
</script>

<template>
  <Card>
    <CardHeader class="-mb-4">
      <CardTitle class="text-3xl">Charts</CardTitle>
    </CardHeader>
    <hr />
    <CardContent>
      <div class="flex outline gap-8">
        <div class="w-2/3 outline my-auto">
            <div>Today</div>

            <div class="h-100 outline"> chart</div>
        </div>

        <div class=" flex-1 space-y-2  outline">
            <div class="p-4 outline">
                <div>Week</div>
                <div class="h-28 outline"></div>
            </div>
            <div class="p-4 outline">
                <div>Month</div>
                <div class="h-28 outline"></div>
            </div>
            <div class="p-4 outline">
                <div>Year</div>
                <div class="h-28 outline"></div>
            </div>
            <div class="p-4 outline">
                <div>Maximum</div>
                <div class="h-28 outline"></div>
            </div>

        </div>
      </div>
    </CardContent>
  </Card>
</template>
