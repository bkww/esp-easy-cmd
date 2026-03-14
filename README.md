# Openclaw-ESP-Easy-MCP-Command
让opencalw能发现所有ESP Easy定义的GPIO设备，并通过自然语言进行控制

# Installation
下载源代码后置于 ~ 目录下，解压后为 ~/esp-easy-cmd
通过本地文件方式安装 openclaw plugins

# Configuration 
修改 opeclaw.json 文件，添加以下内容
  "plugins": {
    "allow": [
      "esp-easy-cmd"
    ],
    "entries": {
      "esp-easy-cmd": {
        "enabled": true,
        "config": {
          "brokerUrl": "mqtt://YOUR-BROKER-ID:1883",
          "clientId": "esp-easy-cmd",
          "devices": [
            {
              "id": "xiaoai",
              "name": "小爱开关",
              "sysname": "ESP_Easy",
              "cmdTopic": "ESP_Easy/cmd",
              "defaultPin": 12,
              "invert": false
            }
            // 增加更多设备
          ]
        }
      }
    }
  }
