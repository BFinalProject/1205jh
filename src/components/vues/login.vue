<template>
  <div>
    <NavHeader />
    <div class="container1" id="container1">
      <div class="form-container1 sign-up-container1">
        <form action="#">
          <br />
          <h1>회원가입하기</h1>
          <div class="social-container1"></div>

          <div class="logins">
            성별&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="inlineRadioOptions"
                id="inlineRadio1"
                value="1"
                style="
                  padding-right: 5px;
                  padding-left: 5px;
                  padding-top: 5px;
                  padding-bottom: 5px;
                "
                v-model="user_gender"
              />
              <label class="form-check-label" for="inlineRadio1">남자</label>
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="inlineRadioOptions"
                id="inlineRadio2"
                value="2"
                style="
                  padding-right: 5px;
                  padding-left: 5px;
                  padding-top: 5px;
                  padding-bottom: 5px;
                "
                v-model="user_gender"
              />
              <label class="form-check-label" for="inlineRadio2">여자</label>
            </div>
          </div>

          <input type="text" placeholder="이름" v-model="user_name" /><br />

          <input type="email" placeholder="아이디" v-model="user_id" /><br />

          <input
            type="password"
            id="password1"
            onchange="passwordreconfirm()"
            placeholder="비밀번호"
            v-model="user_pw"
          /><br />
          <span id="pwConfirm" style="display: none"
            >입력한 글자가 6글자 이상이어야 합니다.</span
          >

          <input
            type="password"
            id="password2"
            onchange="passwordreconfirm()"
            placeholder="비밀번호확인"
          /><br />
          <!-- <span id="re" name="password2" onchange="alert(passwordreconfirm())"></span> -->
          <!-- onchange="alert(passwordreconfirm())" -->

          <span id="pwConfirm2" style="display: none"
            >비밀번호가 불일치 합니다.</span
          >
          <span id="pwConfirm3" style="display: none"
            >비밀번호가 일치 합니다.</span
          >

          <input type="email" placeholder="이메일" v-model="user_mail" /><br />
          <input type="tel" placeholder="휴대폰번호" v-model="user_phonenum" />
          <br />

          <span>체크한 이름: {{ user_gender }}</span>

          <button type="button" class="button1" @click="usersignup()">
            회원가입하기
          </button>
        </form>
      </div>
      <div class="form-container1 sign-in-container1">
        <form action="#">
          <h1>로그인</h1>
          <br />
          <input type="email" placeholder="아이디" />
          <br />
          <input type="password" placeholder="비밀번호" />
          <a href="/findidpw">아이디 혹은 비밀번호를 잊어버리셨나요?</a>

          <div class="login">
            <button
              type="button"
              class="button1"
              style="margin-bottom: 10px"
              onclick="location.href='/main2'"
            >
              로그인
            </button>

            <button type="button" class="kakao" @click="kakaoLogin()">
              <img
                src="../design/imageskakao/kakao_login/ko/kakao_login_medium_narrow.png"
              />
            </button>
          </div>
        </form>
      </div>
      <div class="overlay-container1">
        <div class="overlay">
          <div class="overlay-panel overlay-left">
            <h1>환영합니다!</h1>
            <p>
              우리 서비스를 이용해주셔서 감사합니다
            </p>
            <button type="button" class="button1" id="signIn">
              로그인하기
            </button>
          </div>
          <div class="overlay-panel overlay-right">
            <h1>만나서 반갑습니다!</h1>
            <p>아이디가 없으신가요?</p>
            <button type="button" class="button1" id="signUp">
              회원가입하기
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
@import "./login.css";
body {
  display: flex;
}
</style>
<script>
import NavHeader from "../views/NavHeader.vue";

export default {
  data: function() {
    return {
      user_signup_Information: [],
      user_gender: "",
      user_name: "",
      user_id: "",
      user_pw: "",
      user_mail: "",
      user_phonenum: ""
      // userList:[],
      // updatepassword:[]
    };
  },
  components: {
    NavHeader
  },

  created: function() {
    // console.log("created");
  },
  mounted: function() {
    let vm = this;
    // $('body').class
    // $('body').css({"display": "flex"});
  },
  methods: {
    kakaoLogin() {
      window.Kakao.Auth.login({
        scope: "account_email, gender, age_range",
        success: this.getKakaoAccount
      });
    },
    getKakaoAccount() {
      window.Kakao.API.request({
        url: "/v2/user/me",
        success: res => {
          const kakao_account = res.kakao_account;
          // const nickname = kakao_account.profile.nickname;
          const email = kakao_account.email;
          const gender = kakao_account.gender;
          const age_range = kakao_account.age_range;
          // console.log("nickname", nickname);
          console.log("email", email);
          console.log("gender", gender);
          console.log("age_range", age_range);
          // 로그인 처리 구현
          alert("로그인 성공!");
        },
        fail: error => {
          console.log(error);
        }
      });
      // fnUserInsertList: function(jsonObj) {
      //   this.$sendAxios("/user/insertUserList", jsonObj,
      //     function(resp){
      //         console.log(resp);
      //     });
      // },

      // fnUserUpdatePassword: function(jsonObj) {
      //   this.$sendAxios("/user/updatePassword", jsonObj,
      //     function(resp){
      //          console.log(resp);
      //         });
      //     },
    },
    //로그인 펑션
    usersignup: function() {
      let vm = this;
      // let board_id = vm.$route.query.boardId;
      console.log(vm.user_gender);
      console.log(vm.user_name);
      console.log(vm.user_id);
      console.log(vm.user_pw);
      console.log(vm.user_mail);
      console.log(vm.user_phonenum);

      let send = {
        usergender: vm.user_gender,
        username: vm.user_name,
        userid: vm.user_id,
        userpw: vm.user_pw,
        usermail: vm.user_mail,
        userphonenum: vm.user_phonenum
      };

      let url = "/user/login";

      console.log(url);

      Axios.post(url, send).then(function(response) {
        console.log("stsetsetset");
      });
    }
  }
};
</script>
<style scoped>
h1 {
  font-family: "Do Hyeon", sans-serif;
  font-size: 32px;
  font-weight: 100;
}
button {
  font-family: "Do Hyeon", sans-serif;
  font-size: 20px;
  font-weight: 100;
}
</style>
