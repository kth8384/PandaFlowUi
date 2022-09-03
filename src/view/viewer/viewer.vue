<template>
  <flow-view :code="code" :type="type"></flow-view>
</template>

<script setup lang="ts">
import {useRoute} from "vue-router";
import {ref} from "vue";

const route = useRoute();

const getQuerys = () => {
  return route.query;
};

let codeData = {
  "bpmn": {
    "nodes": [
      {
        "id": "Gateway_34p3k6o",
        "type": "bpmn:exclusiveGateway",
        "x": 620,
        "y": 220,
        "properties": {},
        "text": {
          "x": 620,
          "y": 260,
          "value": "网关"
        }
      },
      {
        "id": "Event_31crj2n",
        "type": "bpmn:startEvent",
        "x": 360,
        "y": 220,
        "properties": {},
        "text": {
          "x": 360,
          "y": 260,
          "value": "开始"
        }
      },
      {
        "id": "Activity_34ajjvv",
        "type": "bpmn:userTask",
        "x": 480,
        "y": 220,
        "properties": {},
        "text": {
          "x": 480,
          "y": 220,
          "value": "用户任务"
        }
      },
      {
        "id": "Activity_3eh37bv",
        "type": "bpmn:userTask",
        "x": 780,
        "y": 160,
        "properties": {},
        "text": {
          "x": 780,
          "y": 160,
          "value": "用户任务"
        }
      },
      {
        "id": "Activity_08ev34c",
        "type": "bpmn:serviceTask",
        "x": 780,
        "y": 300,
        "properties": {},
        "text": {
          "x": 780,
          "y": 300,
          "value": "服务任务"
        }
      },
      {
        "id": "Activity_38con6e",
        "type": "bpmn:endEvent",
        "x": 980,
        "y": 220,
        "properties": {},
        "text": {
          "x": 980,
          "y": 260,
          "value": "结束"
        }
      }
    ],
    "edges": [
      {
        "id": "80378243-59f8-4869-aa10-01c9952aa68c",
        "type": "bpmn:flowLink",
        "sourceNodeId": "Event_31crj2n",
        "targetNodeId": "Activity_34ajjvv",
        "startPoint": {
          "x": 378,
          "y": 220
        },
        "endPoint": {
          "x": 430,
          "y": 220
        },
        "properties": {},
        "pointsList": [
          {
            "x": 378,
            "y": 220
          },
          {
            "x": 478,
            "y": 220
          },
          {
            "x": 330,
            "y": 220
          },
          {
            "x": 430,
            "y": 220
          }
        ]
      },
      {
        "id": "8ff5ccd3-13cb-47a9-b9e8-e46438d5b375",
        "type": "bpmn:flowLink",
        "sourceNodeId": "Activity_34ajjvv",
        "targetNodeId": "Gateway_34p3k6o",
        "startPoint": {
          "x": 530,
          "y": 220
        },
        "endPoint": {
          "x": 595,
          "y": 220
        },
        "properties": {},
        "pointsList": [
          {
            "x": 530,
            "y": 220
          },
          {
            "x": 630,
            "y": 220
          },
          {
            "x": 495,
            "y": 220
          },
          {
            "x": 595,
            "y": 220
          }
        ]
      },
      {
        "id": "9db12c09-2bb2-44cf-b4c0-b962624be4fe",
        "type": "bpmn:flowLink",
        "sourceNodeId": "Gateway_34p3k6o",
        "targetNodeId": "Activity_3eh37bv",
        "startPoint": {
          "x": 645,
          "y": 220
        },
        "endPoint": {
          "x": 730,
          "y": 160
        },
        "properties": {},
        "pointsList": [
          {
            "x": 645,
            "y": 220
          },
          {
            "x": 745,
            "y": 220
          },
          {
            "x": 630,
            "y": 160
          },
          {
            "x": 730,
            "y": 160
          }
        ]
      },
      {
        "id": "7b516f6a-a74f-48cb-879c-ce7ea19c2bbb",
        "type": "bpmn:flowLink",
        "sourceNodeId": "Gateway_34p3k6o",
        "targetNodeId": "Activity_08ev34c",
        "startPoint": {
          "x": 645,
          "y": 220
        },
        "endPoint": {
          "x": 730,
          "y": 300
        },
        "properties": {},
        "pointsList": [
          {
            "x": 645,
            "y": 220
          },
          {
            "x": 745,
            "y": 220
          },
          {
            "x": 630,
            "y": 300
          },
          {
            "x": 730,
            "y": 300
          }
        ]
      },
      {
        "id": "76b51b65-046f-4496-8249-f9a28977f43f",
        "type": "bpmn:flowLink",
        "sourceNodeId": "Activity_3eh37bv",
        "targetNodeId": "Activity_38con6e",
        "startPoint": {
          "x": 830,
          "y": 160
        },
        "endPoint": {
          "x": 980,
          "y": 203
        },
        "properties": {},
        "pointsList": [
          {
            "x": 830,
            "y": 160
          },
          {
            "x": 930,
            "y": 160
          },
          {
            "x": 980,
            "y": 103
          },
          {
            "x": 980,
            "y": 203
          }
        ]
      },
      {
        "id": "d29917c6-d6ef-417a-8cfb-967701c89700",
        "type": "bpmn:flowLink",
        "sourceNodeId": "Activity_08ev34c",
        "targetNodeId": "Activity_38con6e",
        "startPoint": {
          "x": 830,
          "y": 300
        },
        "endPoint": {
          "x": 980,
          "y": 237
        },
        "properties": {},
        "pointsList": [
          {
            "x": 830,
            "y": 300
          },
          {
            "x": 930,
            "y": 300
          },
          {
            "x": 980,
            "y": 337
          },
          {
            "x": 980,
            "y": 237
          }
        ]
      }
    ]
  },
  "nodeRed": {
    nodes: [
      {
        id: 'node_1',
        type: 'start-node',
        x: 220,
        y: 200,
        text: 'start'
      },
      {
        id: 'node_2',
        type: 'fetch-node',
        x: 420,
        y: 200,
        text: 'fetch data'
      },
      {
        id: 'node_3',
        type: 'function-node',
        x: 620,
        y: 200,
        text: 'function'
      },
      {
        id: 'node_4',
        type: 'delay-node',
        x: 420,
        y: 300,
        text: 'delay'
      },
      {
        id: 'node_5',
        type: 'switch-node',
        x: 820,
        y: 200,
        text: 'switch'
      },
      {
        id: 'node_6',
        type: 'function-node',
        x: 1020,
        y: 200,
        text: 'function'
      },
      {
        id: 'node_7',
        type: 'function-node',
        x: 1020,
        y: 300,
        text: 'function'
      }
    ],
    edges: [
      {
        type: 'flow-link',
        sourceNodeId: 'node_1',
        targetNodeId: 'node_2'
      },
      {
        type: 'flow-link',
        sourceNodeId: 'node_2',
        targetNodeId: 'node_3'
      },
      {
        type: 'flow-link',
        sourceNodeId: 'node_3',
        startPoint: {
          x: 680,
          y: 200
        },
        targetNodeId: 'node_4'
      },
      {
        type: 'flow-link',
        sourceNodeId: 'node_4',
        startPoint: {
          x: 370,
          y: 300
        },
        targetNodeId: 'node_2'
      },
      {
        type: 'flow-link',
        sourceNodeId: 'node_3',
        targetNodeId: 'node_5'
      },
      {
        type: 'flow-link',
        sourceNodeId: 'node_5',
        targetNodeId: 'node_6'
      },
      {
        type: 'flow-link',
        sourceNodeId: 'node_5',
        targetNodeId: 'node_7'
      }
    ]
  }
}

const code = ref(getQuerys().type == "bpmn" ? codeData.bpmn : codeData.nodeRed)
const type = ref(getQuerys().type)


</script>

<style scoped>

</style>
