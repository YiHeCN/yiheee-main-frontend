<template>
    <div class="flex flex-row h-full w-full">
        <div class="flex flex-col items-start justify-center w-full">
            <Logo size="36" />
            <h1 class="text-4xl font-bold">做一些有趣的工具</h1>
        </div>
        <div class="flex flex-col items-center justify-center w-full flex-wrap">
            <ul>
                <li class="p-4 flex flex-row items-center justify-between gap-12 hover:bg-gray-100 rounded-md transition-all duration-300"
                v-for="product in products" :key="product.name">
                    <a :href="product.link" target="_blank" style="display: contents;">
                        <div>
                            <p class="text-2xl font-semibold">{{ product.name }}</p>
                            <p class="text-md text-gray-500">{{ product.description }}</p>
                    </div>
                    <div>
                        →
                    </div>
                    </a>
                </li>
            </ul>
        </div>
        
    </div>
</template>

<style scoped>
* {
    user-select: none;
}
</style>
<script setup>
let products = [
    {
        name: 'EZETF',
        description: '美股ETF净值估算和价值发现',
        link: 'https://etf.yihe.ee'
    },
    {
        name: 'EZLifeRec',
        description: '飞书生活记录',
        link: 'https://life.yihe.ee'
    },
    {
        name: 'EZComposition',
        description: 'HTML模板渲染工具',
        link: 'https://composer.yihe.ee'
    },
    {
        name: 'EZData',
        description: '数据散列分布工具',
        link: 'https://ezdata.yihe.ee'
    },
    {
        name: 'Blog',
        description: '我的碎碎念',
        link: 'https://blog.yihe.ee'
    }
]

</script>