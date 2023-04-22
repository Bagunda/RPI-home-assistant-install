### [Dingtian DT-R008 многоканальное умное реле с ethernet и wi-fi - обзор и интеграция в Home Assistant](https://youtu.be/4iDfh65Oxqc)

<a href="https://www.youtube.com/channel/UCcq9onYHbs6go3kDpfBoqhg?sub_confirmation=1" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/subscribe.png" alt="Subscribe" style="height: 71px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

#### Пакадж с объектами MQTT из видео

```yaml

dingtian:

    mqtt:
        switch:    

        - unique_id: dingtian_relay11781_all
          name: dingtian_relay11781_switch_all
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"ON/OFF","idx":"1","status":"ON","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"2","status":"ON","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"3","status":"ON","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"4","status":"ON","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"5","status":"ON","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"6","status":"ON","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"7","status":"ON","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"8","status":"ON","time":"0","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"1","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"2","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"3","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"4","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"5","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"6","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"7","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"8","status":"OFF","time":"0","pass":"0"}'
          optimistic: false
          qos: 0
          retain: false

        - unique_id: dingtian_relay11781_r1
          name: dingtian_relay11781_switch_1
          state_topic: "dingtian/relay11781/out/r1"
          command_topic: "dingtian/relay11781/in/r1"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false
          
        - unique_id: dingtian_relay11781_r2
          name: dingtian_relay11781_switch_2
          state_topic: "dingtian/relay11781/out/r2"
          command_topic: "dingtian/relay11781/in/r2"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false
          
        - unique_id: dingtian_relay11781_r3
          name: dingtian_relay11781_switch_3
          state_topic: "dingtian/relay11781/out/r3"
          command_topic: "dingtian/relay11781/in/r3"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false

        - unique_id: dingtian_relay11781_r4
          name: dingtian_relay11781_switch_4
          state_topic: "dingtian/relay11781/out/r4"
          command_topic: "dingtian/relay11781/in/r4"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false
          
        - unique_id: dingtian_relay11781_r5
          name: dingtian_relay11781_switch_5
          state_topic: "dingtian/relay11781/out/r5"
          command_topic: "dingtian/relay11781/in/r5"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false
          
        - unique_id: dingtian_relay11781_r6
          name: dingtian_relay11781_switch_6
          state_topic: "dingtian/relay11781/out/r6"
          command_topic: "dingtian/relay11781/in/r6"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false
          
        - unique_id: dingtian_relay11781_r7
          name: dingtian_relay11781_switch_7
          state_topic: "dingtian/relay11781/out/r7"
          command_topic: "dingtian/relay11781/in/r7"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false
          
        - unique_id: dingtian_relay11781_r8
          name: dingtian_relay11781_switch_8
          state_topic: "dingtian/relay11781/out/r8"
          command_topic: "dingtian/relay11781/in/r8"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false

        - unique_id: dingtian_relay11781_alljogging_500ms
          name: dingtian_relay11781_switch_alljogging_500ms
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"JOGGING","idx":"1","status":"ON","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"2","status":"ON","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"3","status":"ON","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"4","status":"ON","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"5","status":"ON","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"6","status":"ON","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"7","status":"ON","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"8","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"JOGGING","idx":"1","status":"OFF","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"2","status":"OFF","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"3","status":"OFF","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"4","status":"OFF","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"5","status":"OFF","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"6","status":"OFF","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"7","status":"OFF","time":"5","pass":"0"}
          {"type":"JOGGING","idx":"8","status":"OFF","time":"5","pass":"0"}'
          optimistic: false
          qos: 0
          retain: false


        - unique_id: dingtian_relay11781_r1_jogging_500ms
          name: dingtian_relay11781_switch_1_jogging_500ms
          state_topic: "dingtian/relay11781/out/r1"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"JOGGING","idx":"1","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"JOGGING","idx":"1","status":"OFF","time":"5","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false
          
        - unique_id: dingtian_relay11781_r2_jogging_500ms
          name: dingtian_relay11781_switch_2_jogging_500ms
          state_topic: "dingtian/relay11781/out/r2"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"JOGGING","idx":"2","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"JOGGING","idx":"2","status":"OFF","time":"5","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false
          
        - unique_id: dingtian_relay11781_r3_jogging_500ms
          name: dingtian_relay11781_switch_3_jogging_500ms
          state_topic: "dingtian/relay11781/out/r3"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"JOGGING","idx":"3","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"JOGGING","idx":"3","status":"OFF","time":"5","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r4_jogging_500ms
          name: dingtian_relay11781_switch_4_jogging_500ms
          state_topic: "dingtian/relay11781/out/r4"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"JOGGING","idx":"4","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"JOGGING","idx":"4","status":"OFF","time":"5","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r5_jogging_500ms
          name: dingtian_relay11781_switch_5_jogging_500ms
          state_topic: "dingtian/relay11781/out/r5"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"JOGGING","idx":"5","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"JOGGING","idx":"5","status":"OFF","time":"5","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r6_jogging_500ms
          name: dingtian_relay11781_switch_6_jogging_500ms
          state_topic: "dingtian/relay11781/out/r6"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"JOGGING","idx":"6","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"JOGGING","idx":"6","status":"OFF","time":"5","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r7_jogging_500ms
          name: dingtian_relay11781_switch_7_jogging_500ms
          state_topic: "dingtian/relay11781/out/r7"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"JOGGING","idx":"7","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"JOGGING","idx":"7","status":"OFF","time":"5","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r8_jogging_500ms
          name: dingtian_relay11781_switch_8_jogging_500ms
          state_topic: "dingtian/relay11781/out/r8"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"JOGGING","idx":"8","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"JOGGING","idx":"8","status":"OFF","time":"5","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false           


        - unique_id: dingtian_relay11781_alldelay_5s
          name: dingtian_relay11781_switch_alldelay_5s
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"DELAY","idx":"1","status":"ON","time":"5","pass":"0"}
          {"type":"DELAY","idx":"2","status":"ON","time":"5","pass":"0"}
          {"type":"DELAY","idx":"3","status":"ON","time":"5","pass":"0"}
          {"type":"DELAY","idx":"4","status":"ON","time":"5","pass":"0"}
          {"type":"DELAY","idx":"5","status":"ON","time":"5","pass":"0"}
          {"type":"DELAY","idx":"6","status":"ON","time":"5","pass":"0"}
          {"type":"DELAY","idx":"7","status":"ON","time":"5","pass":"0"}
          {"type":"DELAY","idx":"8","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"JOGGING","idx":"1","status":"OFF","time":"5","pass":"0"}
          {"type":"ON/OFF","idx":"2","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"3","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"4","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"5","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"6","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"7","status":"OFF","time":"0","pass":"0"}
          {"type":"ON/OFF","idx":"8","status":"OFF","time":"0","pass":"0"}'
          optimistic: false
          qos: 0
          retain: false

        - unique_id: dingtian_relay11781_r1_delay_5s
          name: dingtian_relay11781_r1_delay_5s
          state_topic: "dingtian/relay11781/out/r1"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"DELAY","idx":"1","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"1","status":"OFF","time":"0","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false    
          
        - unique_id: dingtian_relay11781_r2_delay_5s
          name: dingtian_relay11781_r2_delay_5s
          state_topic: "dingtian/relay11781/out/r2"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"DELAY","idx":"2","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"2","status":"OFF","time":"0","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r3_delay_5s
          name: dingtian_relay11781_r3_delay_5s
          state_topic: "dingtian/relay11781/out/r3"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"DELAY","idx":"3","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"3","status":"OFF","time":"0","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r4_delay_5s
          name: dingtian_relay11781_r4_delay_5s
          state_topic: "dingtian/relay11781/out/r4"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"DELAY","idx":"4","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"4","status":"OFF","time":"0","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r5_delay_5s
          name: dingtian_relay11781_r5_delay_5s
          state_topic: "dingtian/relay11781/out/r5"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"DELAY","idx":"5","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"5","status":"OFF","time":"0","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r6_delay_5s
          name: dingtian_relay11781_r6_delay_5s
          state_topic: "dingtian/relay11781/out/r6"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"DELAY","idx":"6","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"6","status":"OFF","time":"0","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r7_delay_5s
          name: dingtian_relay11781_r7_delay_5s
          state_topic: "dingtian/relay11781/out/r7"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"DELAY","idx":"7","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"7","status":"OFF","time":"0","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_r8_delay_5s
          name: dingtian_relay11781_r8_delay_5s
          state_topic: "dingtian/relay11781/out/r8"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"DELAY","idx":"8","status":"ON","time":"5","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"8","status":"OFF","time":"0","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_interlock_r1_r2
          name: dingtian_relay11781_switch_r1_r2
          state_topic: "dingtian/relay11781/out/r1"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"ON/OFF","idx":"1","status":"ON","time":"0","pass":"0"},
          {"type":"ON/OFF","idx":"2","status":"OFF","time":"0","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"1","status":"OFF","time":"0","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false          
          
        - unique_id: dingtian_relay11781_interlock_r2_r1
          name: dingtian_relay11781_switch_r2_r1
          state_topic: "dingtian/relay11781/out/r2"
          command_topic: "dingtian/relay11781/in/control"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: '{"type":"ON/OFF","idx":"2","status":"ON","time":"0","pass":"0"},
          {"type":"ON/OFF","idx":"1","status":"OFF","time":"0","pass":"0"}'
          payload_off: '{"type":"ON/OFF","idx":"2","status":"OFF","time":"0","pass":"0"}'
          state_on: "ON"
          state_off: "OFF"
          optimistic: false
          qos: 0
          retain: false           
          
        binary_sensor:

        - unique_id: dingtian_relay11781_i1
          name: dingtian_relay11781_i1
          state_topic: "dingtian/relay11781/out/r1"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          qos: 0          
          
        - unique_id: dingtian_relay11781_i2
          name: dingtian_relay11781_i2
          state_topic: "dingtian/relay11781/out/r2"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          qos: 0          
          
        - unique_id: dingtian_relay11781_i3
          name: dingtian_relay11781_i3
          state_topic: "dingtian/relay11781/out/r3"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          qos: 0            
          
        - unique_id: dingtian_relay11781_i4
          name: dingtian_relay11781_i4
          state_topic: "dingtian/relay11781/out/r4"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          qos: 0           
          
        - unique_id: dingtian_relay11781_i5
          name: dingtian_relay11781_i5
          state_topic: "dingtian/relay11781/out/r5"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          qos: 0           
          
        - unique_id: dingtian_relay11781_i6
          name: dingtian_relay11781_i6
          state_topic: "dingtian/relay11781/out/r6"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          qos: 0           
          
        - unique_id: dingtian_relay11781_i7
          name: dingtian_relay11781_i7
          state_topic: "dingtian/relay11781/out/r7"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          qos: 0           
          
        - unique_id: dingtian_relay11781_i8
          name: dingtian_relay11781_i8
          state_topic: "dingtian/relay11781/out/r8"
          availability:
            - topic: "dingtian/relay11781/out/lwt_availability"
              payload_available: "online"
              payload_not_available: "offline"
          payload_on: "ON"
          payload_off: "OFF"
          qos: 0           
          
        sensor:
        - state_topic: "dingtian/relay11781/out/lwt_availability"
          name: dingtian_relay11781_lwt_availability
          icon: mdi:check-outline

        - state_topic: "dingtian/relay11781/out/ip"
          name: dingtian_relay11781_ip
          icon: mdi:ip

        - state_topic: "dingtian/relay11781/out/mac"
          name: dingtian_relay11781_mac
          icon: mdi:ethernet
    
        - state_topic: "dingtian/relay11781/out/sw_version"
          name: dingtian_relay11781_sw_version
          icon: mdi:update
    
        - state_topic: "dingtian/relay11781/out/hw_version"
          name: dingtian_relay11781_hw_version
          icon: mdi:cpu-64-bit
    
        - state_topic: "dingtian/relay11781/out/sn"
          name: dingtian_relay11781_sn
          icon: mdi:ticket-confirmation-outline 
          

```

____
#### Поддержать развитие проекта *Умный дом с Alex Kvazis*    
<a href="https://www.youtube.com/channel/UCcq9onYHbs6go3kDpfBoqhg/join" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/youtube.png" alt="Youtube Sponsorship" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
<a href="https://www.patreon.com/alex_kvazis" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/patreon-button.png" alt="Patreon Support" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
<a href="https://www.buymeacoffee.com/greatkvazis" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/buymeacoffee.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
<a href="https://www.paypal.com/paypalme/greatkvazis" target="_blank"><img src="https://raw.githubusercontent.com/kvazis/training/master/lessons/img/paypal.png" alt="PayPal Me" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

#### Или перевод любой суммы на -     
* Webmoney - Z243592584952
* BTC - 1Gzr7WQugfnPuWVawu47EiCMTDUBqCAshj
* ETH - 0xa0ce3E29Cf537013649Ae9cdbc08C4853fF91FAc
* LTC - ltc1qs493yk2wk9ywx5h6aruk4p9zm75hx42ekv4ym2
* TRX - TFTCLqvS1tMBwokRHBwz1TCDJ4oD1Z5zPk