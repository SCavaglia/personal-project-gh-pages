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
import { stocksData } from '@/data-mock/projects/stocks'

const chartData = stocksData

type Data = (typeof chartData)[number]

const chartConfig = {
  aapl: {
    label: 'AAPL',
    color: 'var(--chart-1)',
  },
  msft: {
    label: 'MSFT',
    color: 'var(--chart-2)',
  },
  nvda: {
    label: 'NVDA',
    color: 'var(--chart-3)',
  },
  googl: {
    label: 'GOOGL',
    color: 'var(--chart-4)',
  },
} satisfies ChartConfig

const seriesColors = [
  chartConfig.aapl.color,
  chartConfig.msft.color,
  chartConfig.nvda.color,
  chartConfig.googl.color,
]

const tickValues = chartData.filter((_, i) => i % 5 === 0).map((d) => d.date)
</script>

<template>
  <ChartContainer :config="chartConfig">
    <VisXYContainer :data="chartData" :y-domain="[0, undefined]">
      <VisLine
        target="aapl"
        :x="(d: Data) => d.date"
        :y="(d: Data) => d.aapl"
        :color="chartConfig.aapl.color"
        :curve-type="CurveType.Linear"
      />
      <VisLine
        target="msft"
        :x="(d: Data) => d.date"
        :y="(d: Data) => d.msft"
        :color="chartConfig.msft.color"
        :curve-type="CurveType.Linear"
      />
      <VisLine
        target="nvda"
        :x="(d: Data) => d.date"
        :y="(d: Data) => d.nvda"
        :color="chartConfig.nvda.color"
        :curve-type="CurveType.Linear"
      />
      <VisLine
        target="googl"
        :x="(d: Data) => d.date"
        :y="(d: Data) => d.googl"
        :color="chartConfig.googl.color"
        :curve-type="CurveType.Linear"
      />
      <VisAxis
        type="x"
        :x="(d: Data) => d.date"
        :tick-line="false"
        :domain-line="false"
        :grid-line="false"
        :tick-format="
          (d: number) => {
            const date = new Date(d)
            return date.toLocaleDateString('en-US', {
              month: 'short',
              day: 'numeric',
            })
          }
        "
        :tick-values="tickValues"
      />
      <VisAxis type="y" :num-ticks="3" :tick-line="false" :domain-line="false" />
      <ChartTooltip />
      <ChartCrosshair
        :template="componentToString(chartConfig, ChartTooltipContent, { hideLabel: true })"
        :color="(d: Data, i: number) => seriesColors[i]"
      />
    </VisXYContainer>
  </ChartContainer>
</template>
