<template>
  <div id="GoTop" @click="GoTop()" v-show="showButton" class="animated">
    <i class="fa fa-chevron-up"></i>
  </div>
</template>
<script>
export default {
  name: "GoTop",
  data() {
    return {
      showButton: false
    };
  },
  methods: {
    GoTop() {
      (function smoothscroll() {
        var currentScroll =
          document.documentElement.scrollTop || document.body.scrollTop;
        if (currentScroll > 0) {
          window.requestAnimationFrame(smoothscroll);
          window.scrollTo(0, currentScroll - currentScroll / 8); // 加快滚动速度
        }
      })();
    },
    
    // 监听滚动事件，控制按钮显示/隐藏
    handleScroll() {
      const scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
      this.showButton = scrollTop > 300; // 滚动超过300px时显示按钮
    }
  },
  mounted() {
    // 添加滚动事件监听
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    // 移除滚动事件监听
    window.removeEventListener('scroll', this.handleScroll);
  }
};
</script>
<style scoped>
#GoTop {
  width: 50px;
  height: 50px;
  position: fixed;
  right: 30px;
  bottom: 30px;
  z-index: 99999999;
  cursor: pointer;
  background-color: #3498db;
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
  transition: all 0.3s ease;
}

#GoTop:hover {
  background-color: #2980b9;
  transform: translateY(-5px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
}

#GoTop i {
  font-size: 24px;
}

.animated {
  animation: fadeIn 0.5s;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
