<template>
  <div class="page-container">
    <md-button class="md-icon-button md-dense md-raised md-primary" @click="isClicked"></md-button>
    <div class="page-a4">
      <div class="header">
        <h2>上海韦翰斯生物医药科技有限公司</h2>
        <h1>眼科遗传病基因检测报告</h1>
      </div>
      <div class="content">
        <h2 class="sec-title">基本信息</h2>
        <div class="section">
          <div class="md-layout">
            <div class="md-layout-item md-size-25">
              <div class="wfc">
                <span class="wfcl">姓名:</span>
                <md-field md-inline>
                  <md-input :disabled="isDone"></md-input>
                </md-field>
              </div>
            </div>
            <div class="md-layout-item md-size-30">
              <div class="wfc">
                <span class="wfcl">标本类型:</span>
                <md-field md-inline>
                  <md-input :disabled="isDone"></md-input>
                </md-field>
              </div>
            </div>
            <div class="md-layout-item md-size-45">
              <div class="wfc">
                <span class="wfcl">送检单位:</span>
                <md-field md-inline>
                  <md-input :disabled="isDone"></md-input>
                </md-field>
              </div>
            </div>
          </div>
          <div class="md-layout">
            <div class="md-layout-item md-size-25">
              <div class="wfc">
                <span class="wfcl">姓名:</span>
                <md-field md-inline>
                  <md-input v-model="name" :disabled="isDone"></md-input>
                </md-field>
              </div>
            </div>
            <div class="md-layout-item md-size-30">
              <div class="wfc">
                <span class="wfcl">标本类型:</span>
                <md-field md-inline>
                  <md-input v-model="type" :disabled="isDone"></md-input>
                </md-field>
              </div>
            </div>
            <div class="md-layout-item md-size-45">
              <div class="wfc">
                <span class="wfcl">送检单位:</span>
                <md-field md-inline>
                  <md-input ></md-input>
                </md-field>
              </div>
            </div>
          </div>
          <div class="md-layout">
            <div class="md-layout-item md-size-20">
              <div class="wfc">
                <span class="wfcl">姓名:</span>
                <md-field md-inline>
                  <md-input ></md-input>
                </md-field>
              </div>
            </div>
            <div class="md-layout-item md-size-35">
              <div class="wfc">
                <span class="wfcl">标本类型:</span>
                <md-field md-inline>
                  <md-input ></md-input>
                </md-field>
              </div>
            </div>
            <div class="md-layout-item md-size-45">
              <div class="wfc">
                <span class="wfcl">送检单位:</span>
                <md-field md-inline>
                  <md-input ></md-input>
                </md-field>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'app',
  data () {
    return {
      isDone: false,
      selectedEmployee: null,
      name: "黄大华",
      type: "DNA"
    }
  },
  methods: {
    isClicked () {
      this.isDone = !this.isDone;
    }
  }
}
</script>

<style lang="scss">
body {
  background: rgb(204,204,204);
  font-family: 宋体, SimSun, 华文细黑, STXihei, sans-serif;
}

h1, h2, h3, h4, h5 {
  margin: 0;
}

.header{
  text-align: center;

  h1 {
    margin: 16px 0;
    font-size: 34px;
  }
}

.page-container {
  padding-top: 8px;

  >.md-button {
    position: absolute;
    top: 320px;
    right: 20px;
  }

  .page-a4 {
    width: 21cm;
    height: 29.7cm;
    background: white;
    display: block;
    margin: 0 auto;
    margin-bottom: 0.5cm;
    box-shadow: 0 0 0.5cm rgba(0,0,0,0.5);
    padding: 16px 20px;
  }
}

.content {
  padding: 0 40px;

  .sec-title {
    background: #ddd;
    padding: 12px 5px;
  }

  .section {
    padding: 10px 5px;

    .md-layout {
      margin: 10px 0;
    }

    .wfc {
      display: -webkit-flex;
      display: flex;
      align-items: center;
      margin-right: 20px;

      .wfcl {
        margin-right: 20px;
        white-space: nowrap;
      }

      .md-field {
        min-height: 0;
        margin: 0;
        padding-top: 0;

        .md-input {
          line-height: 0px;
          font-size: inherit;
        }

        &.md-disabled:after {
          background-image: none;
          background-color: transparent;
        }
      }
    }
  }
}

</style>
