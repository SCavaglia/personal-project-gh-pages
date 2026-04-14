<script setup lang="ts">
import type { ChartConfig } from '@/components/ui/chart'
import { CurveType } from '@unovis/ts'
import { VisAxis, VisLine, VisXYContainer } from '@unovis/vue'
import {
  ChartContainer,
  ChartCrosshair,
  ChartTooltip,
  ChartTooltipContent,
  componentToString,
} from '@/components/ui/chart'

const description = 'A line chart'

const chartData = [
  { date: new Date('2024-01-01'), desktop: 186 },
  { date: new Date('2024-02-01'), desktop: 305 },
  { date: new Date('2024-03-01'), desktop: 237 },
  { date: new Date('2024-04-01'), desktop: 73 },
  { date: new Date('2024-05-01'), desktop: 209 },
  { date: new Date('2024-06-01'), desktop: 214 },
]

type Data = (typeof chartData)[number]

const chartConfig = {
  desktop: {
    label: 'Desktop',
    color: 'var(--chart-1)',
  },
} satisfies ChartConfig
</script>

<template>
  <ChartContainer :config="chartConfig">
    <VisXYContainer :data="chartData" :margin="{ left: -24 }" :y-domain="[0, undefined]">
      <VisLine
        :x="(d: Data) => d.date"
        :y="(d: Data) => d.desktop"
        :color="chartConfig.desktop.color"
        :curve-type="CurveType.Linear"
      />
      <VisAxis
        type="x"
        :x="(d: Data) => d.date"
        :tick-line="false"
        :domain-line="false"
        :grid-line="false"
        :num-ticks="6"
        :tick-format="
          (d: number) => {
            const date = new Date(d)
            return date.toLocaleDateString('en-US', {
              month: 'short',
            })
          }
        "
        :tick-values="chartData.map((d) => d.date)"
      />
      <VisAxis type="y" :num-ticks="3" :tick-line="false" :domain-line="false" />
      <ChartTooltip />
      <ChartCrosshair
        :template="componentToString(chartConfig, ChartTooltipContent, { hideLabel: true })"
        :color="chartConfig.desktop.color"
      />
    </VisXYContainer>
  </ChartContainer>
</template>
