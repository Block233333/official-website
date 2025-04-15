<template>
  <div id="GoTop" @click="GoTop()" v-show="showButton" class="animated">
    <i class="fa fa-arrow-up"></i>
    <span class="tooltip">返回顶部</span>
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
  width: 55px;
  height: 55px;
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
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.25);
  transition: all 0.3s ease;
  overflow: visible;
}

#GoTop:hover {
  background-color: #2980b9;
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
}

#GoTop:hover .tooltip {
  opacity: 1;
  visibility: visible;
  transform: translateY(0);
}

#GoTop i {
  font-size: 24px;
}

.tooltip {
  position: absolute;
  top: -40px;
  background-color: rgba(0, 0, 0, 0.7);
  color: white;
  padding: 5px 10px;
  border-radius: 4px;
  font-size: 14px;
  opacity: 0;
  visibility: hidden;
  transform: translateY(10px);
  transition: all 0.3s ease;
  white-space: nowrap;
}

.tooltip:after {
  content: '';
  position: absolute;
  bottom: -6px;
  left: 50%;
  margin-left: -6px;
  width: 0;
  height: 0;
  border-left: 6px solid transparent;
  border-right: 6px solid transparent;
  border-top: 6px solid rgba(0, 0, 0, 0.7);
}

.animated {
  animation: bounce 0.5s;
}

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% {
    transform: translateY(0);
  }
  40% {
    transform: translateY(-10px);
  }
  60% {
    transform: translateY(-5px);
  }
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
