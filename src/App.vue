<template>
  <div id="app">
    <!-- 背景 -->
    <div class="background"></div>

    <!-- 主容器 -->
    <div class="main-content">
      <!-- 页眉 -->
      <div class="header">
        <h1>超级翻译工具</h1>
        <p>简单、高效的多语言翻译</p>
      </div>

      <!-- 内容部分 -->
      <div class="content">
        <!-- 输入区域 -->
        <div class="column left">
          <div class="card">
            <div class="language-selection">
              <div class="select-container">
                <label for="sourceLanguageSelect">源语言</label>
                <select v-model="sourceLanguage" id="sourceLanguageSelect" class="form-control">
                  <option value="en">英文</option>
                  <option value="zh-CN">中文（简体）</option>
                  <option value="zh-TW">中文（繁体）</option>
                  <option value="es">西班牙语</option>
                  <option value="fr">法语</option>
                  <option value="de">德语</option>
                  <option value="it">意大利语</option>
                  <option value="pt">葡萄牙语</option>
                  <option value="ru">俄语</option>
                  <option value="ja">日语</option>
                  <option value="ko">韩语</option>
                  <option value="ar">阿拉伯语</option>
                  <option value="nl">荷兰语</option>
                  <option value="tr">土耳其语</option>
                  <option value="el">希腊语</option>
                  <option value="hi">印度语</option>
                  <option value="th">泰语</option>
                  <option value="vi">越南语</option>
                  <option value="pl">波兰语</option>
                  <option value="sv">瑞典语</option>
                  <option value="da">丹麦语</option>
                  <option value="fi">芬兰语</option>
                  <option value="cs">捷克语</option>
                  <option value="hu">匈牙利语</option>
                  <option value="ro">罗马尼亚语</option>
                  <option value="sk">斯洛伐克语</option>
                  <option value="bg">保加利亚语</option>
                  <option value="uk">乌克兰语</option>
                  <option value="sr">塞尔维亚语</option>
                  <option value="hr">克罗地亚语</option>
                  <option value="ms">马来语</option>
                  <option value="id">印尼语</option>
                  <option value="ta">泰米尔语</option>
                  <option value="ml">马拉雅拉姆语</option>
                  <option value="te">泰卢固语</option>
                  <option value="kn">卡纳达语</option>
                  <option value="mr">马拉地语</option>
                  <option value="bn">孟加拉语</option>
                  <option value="pa">旁遮普语</option>
                  <option value="gu">古吉拉特语</option>
                  <option value="or">奥里亚语</option>
                  <option value="as">阿萨姆语</option>
                  <option value="ne">尼泊尔语</option>
                  <option value="si">僧伽罗语</option>
                  <option value="km">高棉语</option>
                  <option value="lo">老挝语</option>
                  <option value="my">缅甸语</option>
                  <option value="tl">他加禄语</option>
                  <option value="jv">爪哇语</option>
                  <option value="uz">乌兹别克语</option>
                  <option value="ky">吉尔吉斯语</option>
                  <option value="az">阿塞拜疆语</option>
                  <option value="am">阿姆哈拉语</option>
                  <option value="haw">夏威夷语</option>
                  <option value="is">冰岛语</option>
                  <option value="eo">世界语</option>
                  <option value="sw">斯瓦希里语</option>
                  <option value="yo">约鲁巴语</option>
                  <option value="zu">祖鲁语</option>
                  <option value="xh">科萨语</option>
                  <option value="af">南非荷兰语</option>
                  <option value="ca">加泰罗尼亚语</option>
                  <option value="eu">巴斯克语</option>
                  <option value="gl">加利西亚语</option>
                  <option value="sq">阿尔巴尼亚语</option>
                  <option value="mk">马其顿语</option>
                  <option value="no">挪威语</option>
                  <option value="fi">芬兰语</option>
                  <option value="sv">瑞典语</option>
                  <option value="lt">立陶宛语</option>
                  <option value="lv">拉脱维亚语</option>
                  <option value="et">爱沙尼亚语</option>
                  <option value="is">冰岛语</option>
                  <option value="hr">克罗地亚语</option>
                  <option value="mt">马耳他语</option>
                  <option value="sl">斯洛文尼亚语</option>
                  <option value="bs">波斯尼亚语</option>
                  <option value="hy">亚美尼亚语</option>
                  <option value="ka">格鲁吉亚语</option>
                  <option value="mr">马拉地语</option>
                  <option value="hy">亚美尼亚语</option>
                  <option value="sq">阿尔巴尼亚语</option>
                </select>
              </div>

              <div class="select-container">
                <label for="targetLanguageSelect">目标语言</label>
                <select v-model="targetLanguage" id="targetLanguageSelect" class="form-control">
                  <option value="en">英文</option>
                  <option value="zh-CN">中文（简体）</option>
                  <option value="zh-TW">中文（繁体）</option>
                  <option value="es">西班牙语</option>
                  <option value="fr">法语</option>
                  <option value="de">德语</option>
                  <option value="it">意大利语</option>
                  <option value="pt">葡萄牙语</option>
                  <option value="ru">俄语</option>
                  <option value="ja">日语</option>
                  <option value="ko">韩语</option>
                  <option value="ar">阿拉伯语</option>
                  <option value="nl">荷兰语</option>
                  <option value="tr">土耳其语</option>
                  <option value="el">希腊语</option>
                  <option value="hi">印度语</option>
                  <option value="th">泰语</option>
                  <option value="vi">越南语</option>
                  <option value="pl">波兰语</option>
                  <option value="sv">瑞典语</option>
                  <option value="da">丹麦语</option>
                  <option value="fi">芬兰语</option>
                  <option value="cs">捷克语</option>
                  <option value="hu">匈牙利语</option>
                  <option value="ro">罗马尼亚语</option>
                  <option value="sk">斯洛伐克语</option>
                  <option value="bg">保加利亚语</option>
                  <option value="uk">乌克兰语</option>
                  <option value="sr">塞尔维亚语</option>
                  <option value="hr">克罗地亚语</option>
                  <option value="ms">马来语</option>
                  <option value="id">印尼语</option>
                  <option value="ta">泰米尔语</option>
                  <option value="ml">马拉雅拉姆语</option>
                  <option value="te">泰卢固语</option>
                  <option value="kn">卡纳达语</option>
                  <option value="mr">马拉地语</option>
                  <option value="bn">孟加拉语</option>
                  <option value="pa">旁遮普语</option>
                  <option value="gu">古吉拉特语</option>
                  <option value="or">奥里亚语</option>
                  <option value="as">阿萨姆语</option>
                  <option value="ne">尼泊尔语</option>
                  <option value="si">僧伽罗语</option>
                  <option value="km">高棉语</option>
                  <option value="lo">老挝语</option>
                  <option value="my">缅甸语</option>
                  <option value="tl">他加禄语</option>
                  <option value="jv">爪哇语</option>
                  <option value="uz">乌兹别克语</option>
                  <option value="ky">吉尔吉斯语</option>
                  <option value="az">阿塞拜疆语</option>
                  <option value="am">阿姆哈拉语</option>
                  <option value="haw">夏威夷语</option>
                  <option value="is">冰岛语</option>
                  <option value="eo">世界语</option>
                  <option value="sw">斯瓦希里语</option>
                  <option value="yo">约鲁巴语</option>
                  <option value="zu">祖鲁语</option>
                  <option value="xh">科萨语</option>
                  <option value="af">南非荷兰语</option>
                  <option value="ca">加泰罗尼亚语</option>
                  <option value="eu">巴斯克语</option>
                  <option value="gl">加利西亚语</option>
                  <option value="sq">阿尔巴尼亚语</option>
                  <option value="mk">马其顿语</option>
                  <option value="no">挪威语</option>
                  <option value="fi">芬兰语</option>
                  <option value="sv">瑞典语</option>
                  <option value="lt">立陶宛语</option>
                  <option value="lv">拉脱维亚语</option>
                  <option value="et">爱沙尼亚语</option>
                  <option value="is">冰岛语</option>
                  <option value="hr">克罗地亚语</option>
                  <option value="mt">马耳他语</option>
                  <option value="sl">斯洛文尼亚语</option>
                  <option value="bs">波斯尼亚语</option>
                  <option value="hy">亚美尼亚语</option>
                  <option value="ka">格鲁吉亚语</option>
                  <option value="mr">马拉地语</option>
                  <option value="hy">亚美尼亚语</option>
                  <option value="sq">阿尔巴尼亚语</option>
                </select>
              </div>
            </div>

            <div class="form-group">
              <label for="textInput">输入文本</label>
              <textarea v-model="text" id="textInput" class="form-control" rows="6" placeholder="请输入文本..."></textarea>
            </div>

            <div class="button-container">
              <button @click="translateText" class="btn btn-primary" :disabled="loading || !text">翻译</button>
            </div>
          </div>
        </div>

        <!-- 结果区域 -->
        <div class="column right">
          <div class="card">
            <h3>翻译结果</h3>
            <p v-if="loading">正在翻译...</p>
            <p v-if="error" class="error">{{ errorMessage }}</p>
            <!-- 翻译结果处理换行 -->
            <p v-if="translatedText" v-html="formattedTranslatedText"></p>
          </div>
        </div>
      </div>
    </div>



  </div>

  <!-- 引入 Footer 组件 -->
  <Footer></Footer>
</template>

<script setup>
import { ref, computed } from 'vue'
import axios from 'axios'
import Footer from './components/Footer.vue'

// 响应式数据
const text = ref('')
const sourceLanguage = ref('en')
const targetLanguage = ref('zh-CN')
const translatedText = ref(null)
const error = ref(false)
const errorMessage = ref('')
const loading = ref(false)

// 翻译函数
const translateText = async () => {
  if (text.value.trim() === '') {
    translatedText.value = null
    return
  }

  if (sourceLanguage.value === targetLanguage.value) {
    error.value = true
    errorMessage.value = '源语言和目标语言相同，请选择不同的目标语言。'
    return
  }

  loading.value = true
  error.value = false
  errorMessage.value = ''
  translatedText.value = null

  try {
    const response = await axios.get(
      'https://api.mymemory.translated.net/get',
      {
        params: {
          q: text.value,
          langpair: `${sourceLanguage.value}|${targetLanguage.value}`,
        },
      }
    )

    if (response.data && response.data.responseData) {
      translatedText.value = response.data.responseData.translatedText
    } else {
      throw new Error('翻译失败，没有返回结果')
    }
  } catch (err) {
    console.error('翻译失败：', err)
    error.value = true
    errorMessage.value = '翻译失败，请稍后再试。'
  } finally {
    loading.value = false
  }
}

// 计算属性，将翻译文本中的换行符 \n 转换为 <br />
const formattedTranslatedText = computed(() => {
  if (!translatedText.value) return ''
  return translatedText.value.replace(/\n/g, '<br />')
})
</script>

<style scoped>
/* 背景 */
.background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, #5c6bc0, #7e57c2);
  /* 渐变色 */
  z-index: -1;
}

/* 主内容区域 */
.main-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  /* 使容器充满整个屏幕 */
  padding: 20px;
  text-align: center;
  color: #fff;
  max-width: 100%;
  overflow: hidden;
}

/* 页眉 */
.header h1 {
  font-size: 3rem;
  color: #fff;
  font-family: 'Roboto', sans-serif;
  margin-bottom: 15px;
}

.header p {
  font-size: 1.5rem;
  color: #fff;
}

/* 内容区域（左右布局） */
.content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 100%;
  max-width: 1200px;
  gap: 30px;
  padding: 20px;
  box-sizing: border-box;
}

/* 左侧和右侧卡片 */
.column {
  flex: 1;
  padding: 20px;
  min-width: 300px;
}

/* 卡片样式 */
.card {
  padding: 20px;
  background-color: #fff;
  border-radius: 12px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  height: 100%;
}

.card h3 {
  font-size: 1.8rem;
  color: #333;
  margin-bottom: 15px;
}

.card p {
  font-size: 1.1rem;
  color: #555;
  word-wrap: break-word;
}

/* 语言选择 */
.language-selection {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}

.select-container {
  width: 48%;
}

.language-selection label {
  font-weight: 600;
  color: #333;
  margin-bottom: 8px;
  display: block;
  font-size: 1rem;
}

.language-selection select {
  padding: 12px;
  width: 100%;
  border-radius: 8px;
  border: 2px solid #ddd;
  background-color: #fafafa;
  font-size: 1rem;
  transition: border-color 0.3s;
}

.language-selection select:focus {
  border-color: #7e57c2;
  outline: none;
}

/* 输入框 */
.form-group {
  margin-bottom: 25px;
}

textarea {
  width: 90%;
  padding: 12px;
  margin-top: 8px;
  border-radius: 8px;
  border: 2px solid #ddd;
  background-color: #fafafa;
  font-size: 1.1rem;
  transition: border-color 0.3s;
  resize: both;
  /* 允许调整大小 */
  max-width: 90%;
  min-width: 90%;
  /* 限制最大宽度为父元素的100% */
  max-height: 300px;
  min-height: 100px;
  /* 限制最大高度，避免过大 */
}

textarea:focus {
  border-color: #7e57c2;
  outline: none;
}

/* 按钮 */
button {
  padding: 12px 24px;
  background-color: #7e57c2;
  color: #fff;
  border: none;
  border-radius: 8px;
  font-size: 1.2rem;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.3s;
}

button:hover {
  background-color: #5c6bc0;
  transform: translateY(-2px);
}

button:disabled {
  background-color: #b0b0b0;
  cursor: not-allowed;
}

/* 错误提示 */
.error {
  margin-top: 20px;
  padding: 15px;
  background-color: #f44336;
  border-radius: 8px;
  color: #fff;
  text-align: center;
}

/* 针对手机的样式 */
@media (max-width: 768px) {

  /* 页眉 */
  .header h1 {
    font-size: 2rem;
  }

  .header p {
    font-size: 1.2rem;
  }

  /* 内容区域（左右布局） */
  .content {
    flex-direction: column;
    gap: 20px;
  }

  .column {
    padding: 10px;
    min-width: 100%;
  }

  .column.right{
    margin-top:10px;
  }

  /* 输入框 */
  textarea {
    width: 90%;
    max-width: 100%;
    min-width: 90%;
    min-height: 120px;
  }

  /* 按钮 */
  button {
    width: 100%;
    padding: 14px;
    font-size: 1.1rem;
  }

  /* 错误提示 */
  .error {
    font-size: 1rem;
    padding: 12px;
  }
}
</style>
