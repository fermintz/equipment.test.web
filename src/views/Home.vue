<template>
  <div class="home fill-height">
    <div class="column column-1 fill-height">
      <div class="head">
        <h2>서버</h2>
      </div>
      <form>
        <v-text-field 
          label="서버주소"
        />
        <v-text-field
          label="서버포트"
        />
        <v-btn 
          outlined
          width="100%"
        >
          서버연결
        </v-btn>
      </form>
    </div>
    <div class="column column-2 fill-height">
      <div class="head">
         <h2>장치</h2>
      </div>

      <div class="add-eq">
        <form>
          <v-text-field label="MAC"></v-text-field>
          <v-btn outlined>장치등록</v-btn>
        </form>
      </div>
      
      <div class="list">
        <h4>장치목록</h4>
        <ul>
          <li v-for="item in 25" :key="item">
            <label>00-IE-68-A5-XX-XX</label>
            <v-btn icon>
              <v-icon>mdi-close</v-icon>
            </v-btn>
          </li>
        </ul>
      </div>
    </div>
    <div class="column column-3 fill-height">
      <div class="head">
        <h2>테스트</h2>
      </div>
      <form>
        <v-text-field 
          label="토픽"
        />
        <v-text-field 
          label="메세지"
        />
        <v-text-field 
          label="테스트시간(분)"
        />
        <v-text-field 
          label="간격(초)"
        />
        <v-btn outlined>다운로드</v-btn>
      </form>

    </div>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: "Home",
};
</script>

<style lang="scss" scoped>

.home{
  display:flex;
  position:relative;
  overflow:hidden;

  .column{
    flex:1;
    padding:30px;

    .head{
      display:flex;
      justify-content: space-between;
      margin-bottom:30px;

      h2{
        font-size:24px;
      }

      h4{
        font-size:18px;
        margin-bottom:10px;
      }
    }
  }

  .column-1{
    .v-btn{
      width:100%;
      min-height:40px;
      margin-top:30px;
      letter-spacing: 0;
    }
  }

  .column-2{
    display:flex;
    flex-direction: column;
    background:#f8f8f8;
    border-left:1px solid #d2d2d2;
    border-right:1px solid #d2d2d2;

    .head{
      display:flex;
    }

    .add-eq{
      margin-bottom:30px;

      .v-btn{
        width:100%;
        min-height:40px;
      }
    }

    .list{
      flex:1;

      h4{margin-bottom:10px;}
      ul{
        padding:0px;
        max-height:40vmin;
        background:#fff;
        border:1px solid #e2e2e2;
        list-style: none;
        overflow-y:scroll;

        li{
          display:flex;
          align-items: center;
          justify-content: space-between;
          border-bottom:1px solid #e2e2e2;
          border-left:0;
          border-right:0px;
          height:50px;
          padding:0 10px;
          background:#fff;
        }
      }
    }
  }

  .column-3{
    .v-btn{
      margin-top:30px;
      min-height:40px;
      width:100%;
    }
  }
}
</style>
