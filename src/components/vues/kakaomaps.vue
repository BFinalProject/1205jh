<template>
  <div>
    <div v-if="onclick == true">
      <!-- <div v-show="onclick"><kakaomaporder/></div> -->
      <button
        class="btn btn-warning"
        type="button"
        data-bs-toggle="offcanvas"
        data-bs-target="#offcanvasScrolling"
        aria-controls="offcanvasScrolling"
        style="position: absolute; z-index: 2;"
      >
        카테고리
      </button>

      <div
        class="offcanvas offcanvas-start show"
        data-b
        bs-scroll="true"
        data-bs-backdrop="false"
        tabindex="-1"
        id="offcanvasScrolling"
        aria-labelledby="offcanvasScrollingLabel"
      >
        <div class="offcanvas-header" display="flex" text-align="center">
          <button type="button" onclick="location.href='/';">
            홈
          </button>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="offcanvas"
            aria-label="Close"
          ></button>
        </div>
        <div class="offcanvas-header" display="flex" text-align="center">
          <div>
            <h4 class="offcanvas-title" id="offcanvasScrollingLabel">
              아래에 해당하는 카테고리를 선택해주세요
            </h4>
          </div>
        </div>
        <!-- 1 -->
        <div>
          <div>
            <input
              type="checkbox"
              class="btn-check"
              name="option1"
              id="option1"
              autocomplete="off"
              value="한식"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option1"
              >한식</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="option2"
              id="option2"
              autocomplete="off"
              value="중식"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option2"
              >중식</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="option3"
              id="option3"
              autocomplete="off"
              value="양식"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option3"
              >양식</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="option4"
              id="option4"
              autocomplete="off"
              value="일식"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option4"
              >일식</label
            >
            <input
              type="checkbox"
              class="btn-check"
              name="option5"
              id="option5"
              autocomplete="off"
              value="기타 음식"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option5"
              >기타 음식</label
            >

            <br />
            <!-- 2 -->

            <input
              type="checkbox"
              class="btn-check"
              name="options2"
              id="option6"
              autocomplete="off"
              value="술집"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option6"
              >술집</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options2"
              id="option7"
              autocomplete="off"
              value="맛집"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option7"
              >맛집</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options2"
              id="option8"
              autocomplete="off"
              value="기념일"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option8"
              >기념일</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options2"
              id="option9"
              autocomplete="off"
              value="가성비"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option9"
              >가성비</label
            >
            <input
              type="checkbox"
              class="btn-check"
              name="options2"
              id="option10"
              autocomplete="off"
              value="뷰"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option10"
              >뷰</label
            >

            <br />
            <!-- 3 -->

            <input
              type="checkbox"
              class="btn-check"
              name="options3"
              id="option11"
              autocomplete="off"
              value="가족"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option11"
              >가족</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options3"
              id="option12"
              autocomplete="off"
              value="애견동반"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option12"
              >애견동반</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options3"
              id="option13"
              autocomplete="off"
              value="색다른"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option13"
              >색다른</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options3"
              id="option14"
              autocomplete="off"
              value="청결"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option14"
              >청결</label
            >
            <input
              type="checkbox"
              class="btn-check"
              name="options3"
              id="option15"
              autocomplete="off"
              value="시끌벅적"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option15"
              >시끌벅적</label
            >

            <br />
            <!-- 4 -->

            <input
              type="checkbox"
              class="btn-check"
              name="options4"
              id="option16"
              autocomplete="off"
              value="한적"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option16"
              >한적</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options4"
              id="option17"
              autocomplete="off"
              value="활동적"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option17"
              >활동적</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options4"
              id="option18"
              autocomplete="off"
              value="고급스런"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option18"
              >고급스런</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options4"
              id="option19"
              autocomplete="off"
              value="감성적"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option19"
              >감성적</label
            >
            <input
              type="checkbox"
              class="btn-check"
              name="options4"
              id="option20"
              autocomplete="off"
              value="이국적"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option20"
              >이국적</label
            >

            <br />
            <!-- 5 -->

            <input
              type="checkbox"
              class="btn-check"
              name="options5"
              id="option21"
              autocomplete="off"
              value="편리한"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option21"
              >편리한</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options5"
              id="option22"
              autocomplete="off"
              value="전통적"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option22"
              >전통적</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options5"
              id="option23"
              autocomplete="off"
              value="모던한"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option23"
              >모던한</label
            >

            <input
              type="checkbox"
              class="btn-check"
              name="options5"
              id="option24"
              autocomplete="off"
              value="편안한"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option24"
              >편안한</label
            >
            <input
              type="checkbox"
              class="btn-check"
              name="options5"
              id="option25"
              autocomplete="off"
              value="이색적"
              v-model="checkedemotion"
            />
            <label style="margin: 10px;" class="btn btn-warning" for="option25"
              >이색적</label
            >
            <br />
            <span>체크한 이름: {{ checkedemotion }}</span>
          </div>
        </div>
        <div style="margin-top: 50px;">
          <button @click="Overlaydata()">선택완료</button>
        </div>
      </div>
    </div>
    <!-- ------------------   order -------------------------------------------------------------------------------- -->

    <!-- <div v-if= "onclick == false"> -->
    <div v-if="onclick == false">
      <button
        class="btn btn-warning"
        type="button"
        data-bs-toggle="offcanvas"
        data-bs-target="#offcanvasScrolling"
        aria-controls="offcanvasScrolling"
        style="position: absolute; z-index: 2;"
      >
        추천장소
      </button>

      <div
        class="offcanvas offcanvas-start show"
        data-bs-scroll="true"
        data-bs-backdrop="false"
        tabindex="-1"
        id="offcanvasScrolling"
        aria-labelledby="offcanvasScrollingLabel"
      >
        <div class="offcanvas-header" display="flex" text-align="center">
          <h4 class="offcanvas-title" id="offcanvasScrollingLabel">
            추천장소를 확인해 주세요!
          </h4>

          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="offcanvas"
            aria-label="Close"
          ></button>
        </div>
        <!-- 1 -->
        <div>
          <div class="row">
            <div class="col-md-12">
              <div id="accordion" class="checkout">
                <div
                  class="panel checkout-step"
                  style="cursor:move;"
                  draggable="true"
                >
                  <div>
                    <span class="checkout-step-number">1</span>
                    <h4 class="checkout-step-title">
                      <a
                        role="button"
                        data-toggle="collapse"
                        data-parent="#accordion"
                        href="#collapseOne"
                      >
                        Phone Number Verification</a
                      >
                    </h4>
                  </div>
                  <div id="collapseOne" class="collapse in"></div>
                </div>
                <div class="panel checkout-step">
                  <div
                    role="tab"
                    id="headingTwo"
                    style="cursor:move;"
                    draggable="true"
                  >
                    <span class="checkout-step-number">2</span>
                    <h4 class="checkout-step-title">
                      <a
                        class="collapsed"
                        role="button"
                        data-toggle="collapse"
                        data-parent="#accordion"
                        href="#collapseTwo"
                      >
                        Delivery Address
                      </a>
                    </h4>
                  </div>
                  <div id="collapseTwo" class="panel-collapse collapse">
                    <div class="checkout-step-body">
                      <div class="checout-address-step">
                        <div class="row">
                          <form class="">
                            <!-- Multiple Radios (inline) -->
                            <div class="form-group">
                              <label
                                class="col-md-12 control-label"
                                for="address"
                              ></label>
                              <div class="col-md-12 ">
                                <label class="radio-inline" for="address-0">
                                  <input
                                    type="radio"
                                    name="address"
                                    id="address-0"
                                    value="Home"
                                    checked="checked"
                                  />
                                  Home
                                </label>
                                <label class="radio-inline" for="address-1">
                                  <input
                                    type="radio"
                                    name="address"
                                    id="address-1"
                                    value="Office"
                                  />
                                  Office
                                </label>
                                <label class="radio-inline" for="address-2">
                                  <input
                                    type="radio"
                                    name="address"
                                    id="address-2"
                                    value="Other"
                                  />
                                  Other
                                </label>
                              </div>
                            </div>
                            <!-- Text input-->
                            <div class="form-group">
                              <div class="col-md-12">
                                <label class="control-label" for="name"
                                  >Name</label
                                >
                                <input
                                  id="name"
                                  name="name"
                                  type="text"
                                  placeholder="Name"
                                  class="form-control input-md"
                                  required=""
                                />
                              </div>
                            </div>
                            <!-- Text input-->
                            <div class="form-group">
                              <label class="col-md-12 control-label" for="flat"
                                >Flat / House / Office No.</label
                              >
                              <div class="col-md-12">
                                <input
                                  id="flat"
                                  name="flat"
                                  type="text"
                                  placeholder="address"
                                  class="form-control input-md"
                                  required=""
                                />
                              </div>
                            </div>
                            <!-- Text input-->
                            <div class="form-group">
                              <label
                                class="col-md-12 control-label"
                                for="street"
                                >Street / Society / Office Name</label
                              >
                              <div class="col-md-12">
                                <input
                                  id="street"
                                  name="street"
                                  type="text"
                                  placeholder="Street Address"
                                  class="form-control input-md"
                                />
                              </div>
                            </div>
                            <!-- Text input-->
                            <div class="form-group">
                              <label
                                class="col-md-12 control-label"
                                for="Locality"
                                >Locality</label
                              >
                              <div class="col-md-12">
                                <input
                                  id="Locality"
                                  name="Locality"
                                  type="text"
                                  placeholder="Ahmedabad"
                                  class="form-control input-md"
                                  required=""
                                />
                              </div>
                            </div>
                            <!-- Button -->
                            <div class="form-group">
                              <div class="col-md-12">
                                <button
                                  id="singlebutton"
                                  name="singlebutton"
                                  class="btn btn-primary"
                                >
                                  Save
                                </button>
                              </div>
                            </div>
                          </form>
                        </div>
                      </div>
                      <a
                        class="collapsed btn btn-default"
                        role="button"
                        data-toggle="collapse"
                        data-parent="#accordion"
                        href="#collapseThree"
                      >
                        Next
                      </a>
                    </div>
                  </div>
                </div>
                <div class="panel checkout-step">
                  <div
                    role="tab"
                    id="headingThree"
                    style="cursor:move;"
                    draggable="true"
                  >
                    <span class="checkout-step-number">3</span>
                    <h4 class="checkout-step-title">
                      <a
                        class="collapsed"
                        role="button"
                        data-toggle="collapse"
                        data-parent="#accordion"
                        href="#collapseThree"
                      >
                        Time & Date
                      </a>
                    </h4>
                  </div>
                  <div id="collapseThree" class="panel-collapse collapse">
                    <div class="checkout-step-body">
                      <div class="row">
                        <div class="form-group">
                          <label class="col-md-12 control-label" for="time"
                            >Time</label
                          >
                          <div class="col-md-12">
                            <div class="radio">
                              <label for="time-0">
                                <input
                                  type="radio"
                                  name="time"
                                  id="time-0"
                                  value="8:00 - 9:00"
                                  checked="checked"
                                />
                                8:00 - 9:00
                              </label>
                            </div>
                            <div class="radio">
                              <label for="time-1">
                                <input
                                  type="radio"
                                  name="time"
                                  id="time-1"
                                  value="10:00 - 11:00"
                                />
                                10:00 - 11:00
                              </label>
                            </div>
                            <div class="radio">
                              <label for="time-2">
                                <input
                                  type="radio"
                                  name="time"
                                  id="time-2"
                                  value="12:00 - 1:00"
                                />
                                12:00 - 1:00
                              </label>
                            </div>
                            <div class="radio">
                              <label for="time-3">
                                <input
                                  type="radio"
                                  name="time"
                                  id="time-3"
                                  value="1:00 - 2:00"
                                />
                                1:00 - 2:00
                              </label>
                            </div>
                          </div>
                        </div>
                      </div>
                      <a
                        class="collapsed btn btn-default"
                        role="button"
                        data-toggle="collapse"
                        data-parent="#accordion"
                        href="#collapseFour"
                      >
                        Next
                      </a>
                    </div>
                  </div>
                </div>
                <div class="panel checkout-step">
                  <div
                    role="tab"
                    id="headingFour"
                    style="cursor:move;"
                    draggable="true"
                  >
                    <span class="checkout-step-number">4</span>
                    <h4 class="checkout-step-title">
                      <a
                        class="collapsed"
                        role="button"
                        data-toggle="collapse"
                        data-parent="#accordion"
                        href="#collapseFour"
                      >
                        Payment
                      </a>
                    </h4>
                  </div>
                  <div id="collapseFour" class="panel-collapse collapse">
                    <div class="checkout-step-body">
                      Payment Mode
                      <a href="#" class="btn btn-default"
                        >Proccess to payment</a
                      >
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        Credit by
        <a href="http://jituchauhan.com/" target="_blank"> jitu chauhan</a>
        <div style="margin-top: 50px;">
          <button @click="hideMarkers3()">마커 선택</button>
          <button @click="hideMarkers()">마커 삭제</button>
          <button @click="hideMarkers2()">마커 삭제2</button>
        </div>
      </div>
    </div>

    <div id="map" style="height:100vh;"></div>
  </div>
</template>

<script>
import Axios from "axios";
import kakaomaporder from "../../kakaomapview/kakaomaporder.vue";
import $ from "jquery";
export default {
  name: "kakaomaps",
  el: "#sel",
  components: {
    kakaomaporder
  },
  data() {
    return {
      datas: [],
      mapOption: {},
      map: [],
      marker: {},
      clusterer: {},
      markers: {},
      onclick: true,
      resetmarker: [],
      checkedemotion: [],
      markerPosition: [],
      markeris: [],
      polyline: []
    };
  },

  mounted() {
    let vm = this;
    let mapContainer = document.getElementById("map");
    vm.mapOption = {
      //지도를 생성할 때 필요한 기본 옵션
      center: new kakao.maps.LatLng(33.450701, 126.570667), //지도의 중심좌표.
      level: 5 //지도의 레벨(확대, 축소 정도)
    };
    vm.map = new kakao.maps.Map(mapContainer, vm.mapOption);

    vm.clusterer = new kakao.maps.MarkerClusterer({
      map: vm.map,
      markers: null,
      gridSize: 35,
      averageCenter: true,
      minLevel: 6,
      disableClickZoom: true,
      styles: [
        {
          width: "53px",
          height: "52px",
          background: "url(cluster.png) no-repeat",
          color: "#fff",
          textAlign: "center",
          lineHeight: "54px"
        }
      ]
    });
  },
  methods: {
    Overlaydata: function() {
      let vm = this;

      vm.map.relayout();
      let data = [
        { x: 37.482802136930516, y: 126.79564879005665 },
        { x: 37.483987091628535, y: 126.7830868366494 },
        { x: 37.46851044224279, y: 126.797275939562 }
      ];
      (vm.datas = []), (vm.markeris = data);
      console.log(vm.markeris);
      // let imageSrc = 'https://t1.daumcdn.net/localimg/localimages/07/mapapidoc/marker_red.png', // 마커이미지의 주소입니다
      // let imageSrc ="../design/markerimges/img1.png", // 마커이미지의 주소입니다
      let imageSrc =
          "https://t1.daumcdn.net/localimg/localimages/07/mapapidoc/marker_red.png", // 마커이미지의 주소입니다
        imageSize = new kakao.maps.Size(64, 69), // 마커이미지의 크기입니다
        imageOption = { offset: new kakao.maps.Point(27, 69) };
      // 마커이미지의 옵션입니다. 마커의 좌표와 일치시킬 이미지 안에서의 좌표를 설정합니다.

      // 마커의 이미지정보를 가지고 있는 마커이미지를 생성합니다
      let markerImage = new kakao.maps.MarkerImage(
        imageSrc,
        imageSize,
        imageOption
      );

      let bounds = new kakao.maps.LatLngBounds();

      vm.markeris.forEach(element => {
        vm.markerPosition = new kakao.maps.LatLng(element.x, element.y); // 마커가 표시될 위치입니다
        console.log(vm.markerPosition);
        let iwRemoveable = true;
        // 마커를 생성합니다
        vm.marker = new kakao.maps.Marker({
          position: vm.markerPosition,
          image: markerImage, // 마커이미지 설정
          removable: iwRemoveable,
          id: "tests"
        });

        let mapmovedata = bounds.extend(vm.markerPosition);
        // 마커가 지도 위에 표시되도록 설정합니다
        //this.clusteredr.clear(marker);
        //marker.setMap(null);image.png

        vm.marker.setMap(vm.map);
        vm.map.setBounds(mapmovedata);

        // 커스텀 오버레이에 표출될 내용으로 HTML 문자열이나 document element가 가능합니다
        let content =
          `<div class= 'customoverlay'>` +
          '  <a href="https://map.kakao.com/link/map/11394059" target="_blank">' +
          '    <span class="title">구구공원</span>' +
          "  </a>" +
          "</div>";

        // 커스텀 오버레이가 표시될 위치입니다
        let position = new kakao.maps.LatLng(element.x, element.y);
        // ㄱㄷ 잠만 부장온다
        // 커스텀 오버레이를 생성합니다아
        let customOverlay = new kakao.maps.CustomOverlay({
          map: vm.map,
          position: position,
          content: content,
          yAnchor: 1
        });

        vm.datas.push(new kakao.maps.LatLng(element.x, element.y));
        // vm.polyline.setMap(null);
        vm.polyline = new kakao.maps.Polyline({
          path: vm.datas, // 선을 구성하는 좌표배열 입니다
          strokeWeight: 5, // 선의 두께 입니다
          strokeColor: "#FFAE00", // 선의 색깔입니다
          strokeOpacity: 0.7, // 선의 불투명도 입니다 1에서 0 사이의 값이며 0에 가까울수록 투명합니다
          strokeStyle: "solid", // 선의 스타일입니다
          zIndex: 4
        });

        //polyline.setMap(null);
        vm.polyline.setMap(vm.map);
      });
      console.log(vm.onclick);
      vm.onclick = false;
      console.log(vm.onclick);
      // this.onclick = !this.onclick;
    },

    // click: function () {
    //     let vm = this;
    //     var i

    //     for (i = 0; i > vm.markers.length; i++) {
    //         vm.map.setMap(vm.markers[i]);
    //     }
    // }
    hideMarkers: function() {
      let vm = this;
      vm.markeris.clear = function() {
        if (vm.markeris.length > 0) {
          for (let i = 0; i < vm.markeris.length; i++) {
            vm.markerPosition[i].setMap(null);
          }
        }
      };
      vm.markeris.clear = function() {
        if (vm.markeris) vm.markeris.clear(vm.map);

        console.log(vm.marker.position);
        console.log(vm.markerPosition);
        // console.log(vm.markerPosition);
        // let getmarker;
        // for(let i=0; i < vm.marker.length; i++){
        //     getmarker = vm.marker[i],
        //     getmarker = null
        //     console.log(getmarker);
        // }

        // console.log(vm.marker)
        // vm.marker.setMap(vm.map);
        // marker.setMap(vm.map);
      };
    },
    hideMarkers2: function() {
      vm.markeris = document.document.getElementById("gs");
      console.log($("gs"));
      let vm = this;
      $("gs").remove();
    },
    hideMarkers3: function() {
      let vm = this;
      console.log(vm.onclick);

      $(".customoverlay")
        .parent()
        .empty();
      $(
        "img[src='https://t1.daumcdn.net/localimg/localimages/07/mapapidoc/marker_red.png']"
      )
        .parent()
        .empty();
      $("path[id*='daum-maps-shape-']")
        .parent()
        .empty();

      vm.onclick = true;
    }
  }
};
</script>
<style>
.customoverlay {
  position: relative;
  bottom: 85px;
  border-radius: 6px;
  border: 1px solid #ccc;
  border-bottom: 2px solid #ddd;
  float: left;
}

.customoverlay:nth-of-type(n) {
  border: 0;
  box-shadow: 0px 1px 2px #888;
}

.customoverlay a {
  display: block;
  text-decoration: none;
  color: #000;
  text-align: center;
  border-radius: 6px;
  font-size: 14px;
  font-weight: bold;
  overflow: hidden;
  background: #d95050;
  background: #d95050
    url(https://t1.daumcdn.net/localimg/localimages/07/mapapidoc/arrow_white.png)
    no-repeat right 14px center;
}

.customoverlay .title {
  display: block;
  text-align: center;
  background: #fff;
  margin-right: 35px;
  padding: 10px 15px;
  font-size: 14px;
  font-weight: bold;
}

.customoverlay:after {
  content: "";
  position: absolute;
  margin-left: -12px;
  left: 50%;
  bottom: -12px;
  width: 22px;
  height: 12px;
  background: url("https://t1.daumcdn.net/localimg/localimages/07/mapapidoc/vertex_white.png");
}

#map {
  width: 100%;
  height: 96vh;
}

.button-group {
  margin: 10px 0px;
}

button {
  margin: 0 3px;
}

.box {
  margin: 30px 50px 30px 50px;
}

.offcanvas-start {
  width: 490px;
}

.offcanvas {
  text-align: center;
  justify-content: center;
}

.offcanvas-header {
  text-align: center;
  justify-content: space-between;
  margin-bottom: 1.5rem;
}

a {
  font-family: "Do Hyeon", sans-serif;
  font-size: 20px;
}

h4 {
  font-family: "Do Hyeon", sans-serif;
  font-size: 20px;
}

button {
  font-family: "Do Hyeon", sans-serif;
  font-size: 20px;
}

label,
span {
  font-family: "Do Hyeon", sans-serif;
}
</style>
