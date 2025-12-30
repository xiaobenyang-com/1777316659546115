# 图表工具服务 Quick Chart

一个基于Model Context Protocol (MCP)的服务器，提供与Quick Chart交互的标准化接口，支持图表生成和管理。
A server based on Model Context Protocol (MCP), providing a standardized interface for interacting with Quick Chart and supporting chart generation and management.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| GetChartImgLink | To draw chart and get chart image link by parameters, and parameter grammar follows Quick Chart API (quickchart.io). |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659546115](https://mcp.xiaobenyang.com/inspector/1777316659546115)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659546115](https://mcp.xiaobenyang.com/inspector/1777316659546115)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "图表工具服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659546115/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "图表工具服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659546115/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "图表工具服务": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659546115",
          },
          "transport": "stdio"
        }
      }
}

```
