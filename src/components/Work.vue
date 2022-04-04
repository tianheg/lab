<script setup>
import SingleWork from './SingleWork.vue'
import dayjs from 'dayjs'

import HtmlIcon from './icons/IconHtml.vue'
import MapIcon from './icons/IconMap.vue'
import RandomIcon from './icons/IconRandom.vue'
import XiaomiIcon from './icons/IconXiaomi.vue'

function formatDate(d) {
  const date = dayjs(d)
  // if (date.year() === dayjs().year())
  //     return date.format('MMM D');
  return date.format('MMM D, YYYY')
}
// formatDate() === now
</script>

<template>
  <SingleWork>
    <template #icon>
      <MapIcon />
    </template>
    <template #time>
      {{ formatDate('2022-03-14') }} - {{ formatDate() }}
    </template>
    <template #heading>杭州互联网公司地图</template>

    <a href="https://tianheg.github.io/hangzhou-it-map/">主页</a>，<a
      href="https://github.com/tianheg/hangzhou-it-map"
      >仓库</a
    >
  </SingleWork>

  <SingleWork>
    <template #icon>
      <RandomIcon />
    </template>
    <template #time>
      {{ formatDate('2021-12-14') }} - {{ formatDate('2022-03-04') }}
    </template>
    <template #heading>随机文章</template>

    <a href="https://tianheg.github.io/random-blog/">主页</a>，<a
      href="https://github.com/tianheg/random-blog"
      >仓库</a
    >
  </SingleWork>

  <SingleWork>
    <template #icon>
      <XiaomiIcon />
    </template>
    <template #time>
      {{ formatDate('2021-08-25') }} - {{ formatDate('2021-09-15') }}
    </template>
    <template #heading>生产实习-小米后台管理系统</template>

    <a href="https://www.yidajiabei.xyz/posts/xiaomi-system/">文章</a>，<a
      href="https://github.com/tianheg/xiaomi2"
      >仓库</a
    >
  </SingleWork>

  <SingleWork>
    <template #icon>
      <HtmlIcon />
    </template>
    <template #time>
      {{ formatDate('2021-05-08') }} - {{ formatDate() }}
    </template>
    <template #heading>50projects50days</template>

    每天一个项目，用 HTML、CSS、JavaScript 完成，<a
      href="https://tianheg.github.io/50projects50days/"
      >主页</a
    >，<a href="https://github.com/tianheg/50projects50days">仓库</a>
  </SingleWork>

  <SingleWork>
    <template #icon>
      <XiaomiIcon />
    </template>
    <template #time>
      {{ formatDate('2021-05-08') }} - {{ formatDate('2021-05-12') }}
    </template>
    <template #heading>小米官网</template>

    静态页面，<a href="https://tianheg.github.io/xiaomi/" target="_blank"
      >主页</a
    >，<a href="https://github.com/tianheg/xiaomi" target="_blank">仓库</a>
  </SingleWork>
</template>
