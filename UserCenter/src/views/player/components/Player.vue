<template>
    <div id="window">
        <div id="view">
            <div id="player-box-container" class="col-md-12 col-xs-12 player-box">
                <div id="mianPlayerBox" style="height: 100%;">
                </div>
                <div id="auxPlayerBox">
                </div>
                <div id="audioPlayerBox">
                </div>
            </div>
            <div class="view-bottom">

            </div>
        </div>
    </div>
</template>

<script>
    import LMC from '../common/lmc.js' 
    
    export default {
        data(){
            return {
                
            }
        },
        computed:{},
        created(){
            
            document.getElementsByTagName('title')[0].innerHTML = '视频播放'
            if(window.location.href.split('?')[1]){
                this.initPlayer(this.getParams())
            }
          
        },
        mounted(){
            
        },
        methods: {
            getParams(){
                let initParams = {}
                window.location.href.split('?')[1].split('&').map((item) => {
                    initParams[item.split('=')[0]] = item.split('=')[1]
                })
                return initParams
            },
            initPlayer(params){
                LMC.init({
                    appConfig: {
                        // 应用配置
                        lmcServer: "https://lmc.91haoke.com/core",
                        cacheJs: true, // 是否缓存JavaScript文件,默认不缓存
                        appId: params.appId, // 应用id
                        appSign: params.appSign, // 应用授权签名,
                        expire: params.expire, //鉴权到期时间
                        random: params.random, //鉴权随机字符串
                        debug: true, //是否输出调试信息
                        errorPage: null, // 加载错误页面,
                        repeatPage: null, // 重复登录错误页面,
                        timeoutPage: null, // 鉴权超时错误页面
                        volume: 80 // 默认音量
                    },

                    liveConfig: {
                        // 直播配置
                        roomId: params.roomId // 直播间id
                    },

                    userConfig: {
                        // 用户配置
                        userId: params.userId, // 用户身份标识
                        nickname: params.nickname, // 用户身份标识
                        headerUrl: params.headerUrl, // 用户头像路径
                        role: params.role, // ['teacher','assistant','student']  用户权限，可以自行扩展
                        subGroupId: params.subGroupId, //用户分组id,如果所属多个分则用逗号分隔,如果属于全部组则subGroupId为ALL
                        onlyGroupMsg: true //设置用户是否只显示组内消息
                    },

                    modules: {
                        //模块配置
                        notify: {
                            //初始化完成
                            onInitCompleted: function(self) {
                                console.log(self)
                            }
                        }
                    }
                })
            }
        }
    }
</script>

<style lang="less" scoped>
    // #window{
    //     position: absolute;
    //     width: 100%;
    //     height: 100%;
    //     background: #fff;
    // }
</style>


