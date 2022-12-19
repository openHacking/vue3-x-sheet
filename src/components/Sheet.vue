<script setup lang="ts">
import { onMounted } from "vue";

onMounted(() => {
  const settings = {
    // 工作簿配置
    workConfig: {
      // 主体配置
      body: {
        // 工作表主体配置
        sheets: [
          {
            // 工作表名称
            name: "sheet1",
            // 表格配置
            tableConfig: {
              // 表格数据，二维数组
              data: [
                [
                  {
                    // 文本内容
                    text: "Text1",
                  },
                  {
                    // 文本内容
                    text: "Text2",
                  },
                ],
              ],
              // 合并单元格
              merge: { merges: ["A2:B3"] },
            },
          },
        ],
      },
    },
  };

  new window.XSheet("#demo", settings);
});
</script>

<template>
  <div id="demo"></div>
</template>

<style scoped>
#demo {
  width: 100%;
  height: 100%;
}
</style>
