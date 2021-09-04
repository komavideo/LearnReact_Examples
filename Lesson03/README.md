React.js 播放视频啦！我也做个 Youtube 吧！
======================================

## 知识点

* 使用 React.js 播放视频

## 官网

https://github.com/CookPete/react-player

## 实战演习

+ 使用 react-player 播放视频

## 操作步骤

### 使用 react-player 播放视频

```bash
$ npx create-react-app komavideoweb
$ cd komavideoweb
$ npm install react-player --save
$ nano App.js
```

### App.js

```jsx
import React, { useState } from 'react';
import ReactPlayer from 'react-player';

import Header from './components/Header';

function App() {
    const [playUrl, setPlayUrl] = useState('https://www.youtube.com/watch?v=QVrip_m0c8Y')
    const [isPlaying, setIsPlaying] = useState(false)

    return (
        <div>
            <Header></Header>
            <div className="py-2 px-4">
                <ReactPlayer url={playUrl} controls='true' playing={isPlaying} />
                <div className="py-1">
                    <button className="btn btn-danger btn-lg" onClick={() => setIsPlaying(!isPlaying)}>
                        {isPlaying ? 'Stop' : 'Play'}
                    </button>
                </div>
            </div>
            <hr />
            <div className="py-2 px-4">
                <button className="btn btn-primary mx-1" onClick={() => setPlayUrl("https://www.youtube.com/watch?v=Mjfa2qsTohU")}>微服务开发</button>
                <button className="btn btn-success mx-1" onClick={() => setPlayUrl("https://www.youtube.com/watch?v=oBwWFiHEr94")}>RDS MySQL</button>
                <button className="btn btn-info    mx-1" onClick={() => setPlayUrl("https://www.youtube.com/watch?v=Ja-sBN8svyo")}>JS 解构</button>
                <button className="btn btn-warning mx-1" onClick={() => setPlayUrl("https://www.youtube.com/watch?v=2BHa9oAd3Fk")}>AWS认证之路</button>
            </div>
        </div>
    );
}

export default App;
```

## 课程文件

https://github.com/komavideo/LearnReact_Examples

## 课程文件分享 - 小马部落Discord会员区

https://discord.gg/VSKw72P

## 小马视频频道

http://komavideo.com

## 深学AWS

https://deeplearnaws.com
