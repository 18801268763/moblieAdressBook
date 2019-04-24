<template>
  <div id="app">
    <mt-header title="手机通讯录">
      <mt-button icon="back" slot="left">返回</mt-button>
      <mt-button icon="more" slot="right"></mt-button>
    </mt-header>

    <mt-index-list>
        <mt-index-section v-for="item in items" :index="item.index">
          <mt-cell v-for="user in item.users" :title="user.name"></mt-cell>
        </mt-index-section>
    </mt-index-list>
  </div>
</template>

<script>
  let userData = [
  {"index":"A", "users": [
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"}
      ]
    },
    {"index":"B", "users": [
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"}
      ]
    },{"index":"C", "users": [
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"}
      ]
    },{"index":"D", "users": [
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"},
          {"name": "a1","tel": "18801268763"}
      ]
    }
  ];
export default {
  name: 'app',
  data () {
    return {
      items: userData
    }
  }
}
</script>

<style>
*{
  margin:0;
  padding:0;
}

.mint-indexsection-index{
  color: red;
}
</style>
