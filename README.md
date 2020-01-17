# graduate


<h3>说明:</h3>
<ul>
      <li>id都为int类型，其他字段都为string类型！</li>
      <li>status：  0表示成功，1表示失败</li>
      <li>message:具体的消息信息</li>
    </ul>
<body>
 <h4>获取验证码</h4>    
       <span>接口：/verify</span><br/>
       <span>请求：GET</span><br/>
       <span>参数：stu_phone   手机号</span><br/>
       <span>调用形式：/verify?stu_phone=15690580872</span><br/>
       
       成功返回值：
                {
                    status:0,
                    stu_phone,//用户收到的验证码
                    message:'请求成功'
                }
              
            
       错误返回值:
            {
                   status:1,
                   message:errorMessage
            }    
            
----------------------------------------------------- 学生 ----------------------------------------------------------

<h4>学生注册</h4>
       <span>接口：/register_stu</span><br/>
       <span>请求：POST</span><br/>
       <span>参数：stu_phone  手机号<br/>
                   stu_password  密码
        </span><br/>
       <span>调用形式：/register_stu</span><br/>
        
       成功返回值：
                {
                    status:0,
                    info    : 'OK',
                    message:'注册成功'
                }
              
            
       错误返回值:
                {
                   status  : 1,
                info    : 'error',
                message:'注册失败'
            }    
                   


  <h4>学生登陆</h4>
       <span>接口：/login</span><br/>
       <span>请求：POST</span><br/>
       <span>参数：stu_phone  手机号<br/>
                 stu_password  密码
       </span><br/>
       <span>调用形式：/login</span><br/>

       成功返回值：
                {
                    status:0,
                    info    : 'OK',
                    tokenID:(用户tokenID,唯一标识)
                    information 用户的所有资料
                    message:'密码匹配正确'
                }
              
            
       错误返回值:{
                    status:1,
                    info    : 'error',
                    message:'密码匹配错误'
            }    
            


  <h4>更新用户资料</h4>    
        <span>接口：/updata_stu</span><br/>
        <span>请求：POST</span><br/>
        <span>调用形式：/updata_stu</span><br/>
        <span>参数：
         stu_id  查找学生用<br/>
         stu_name<br/>
         stu_age <br/>
         stu_sex <br/>
         stu_grade
        </span><br/>

        成功返回值：
                {
                    status:0,
                    message:'修改成功'
                }
              
            
        错误返回值:{
                   status:1,
                   message:errorMessage
            }    
            


  <h4>获取用户资料</h4>
        <span>接口：/showdata_stu</span><br/>
        <span>请求：get</span><br/>
        <span>调用形式：/showdata_stu?stu_id=?</span><br/>
        <span>参数：stu_id</span><br/>
            
        成功返回值：
                {
                     array[object]
                }
              
            
        错误返回值:{
                   status:1,
                   message:errorMessage
            }    
            


  <h4>头像上传</h4>
        <span>接口：/upload_head</span><br/>
        <span>请求：post</span><br/>
        <span>参数：stu_id 用户id<br/>
                    file文件<br/>
        </span><br/>
            
        成功返回值：
                {
                    status:0,
                    headurl:url,
                    info:'ok',
                    message:'成功'
                }
              
            
        错误返回值:{
                   status:1,
                   message:errorMessage
            }    


 <h4>更改密码</h4>
        <span>接口：/forget</span><br/>
        <span>请求：POST</span><br/>
        <span>参数：
            stu_phone 用户手机号 int<br/>
            stu_password 新密码 int<br/>
        </span><br/>
        <span>调用形式：/forget</span><br/>

        成功返回值：
                {
                    status:0,
                    message:'修改成功'
                }
              
            }
        错误返回值:{
                   status:1,
                   message:errorMessage
            }    
            );
            

  <h4>找回密码发送验证码</h4>
        <span>接口：/findVerify</span><br/>
        <span>请求：get</span><br/> 
        <span>参数：
            stu_phone 用户手机号 int
        </span><br/>
        <span>调用形式：findVerify？stu_phone = ?</span><br/>

        成功返回值：
                {
                    status:0,
                    stu_phone,//用户收到的验证码
                    message:'请求成功'
                }
              
            }
        错误返回值:{
                   status:1,
                   message:errorMessage
            }    
            );


 <h4>得到自己的下载记录</h4>
        <span>接口：/getOwnLoad</span><br/>
        <span>请求：get</span><br/>
        <span>参数：stu_id</span><br/>
          
        成功返回值：
              array[object]
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );

   <h4>得到自己的错题</h4>
        <span>接口：/getOwnFalse</span><br/>
        <span>请求：get</span><br/>
        <span>参数：stu_id</span><br/>
          
        成功返回值：
              array[object]
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );


   <h4>得到自己的学习记录</h4>
        <span>接口：/getOwnLearn</span><br/>
        <span>请求：get</span><br/>
        <span>参数：stu_id</span><br/>
          
        成功返回值：
              array[object]
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );

----------------------------------------------------- 信息分享 ----------------------------------------------------------

  <h4>获得视频</h4>
        <span>接口：/select_video</span><br/>
        <span>请求：get</span><br/>
        <span>参数：无调用参数</span><br/>
        <span>调用形式：/select_video</span><br/>
        
         成功返回值：
                {
                array[object]  //返回一个数组，每个视频的信息为数组中的一个对象
                } 
              
            


   <h4>获得笑话</h4>
        <span>接口：/select_smile</span><br/>
        <span>请求：get</span><br/>
        <span>参数：无调用参数</span><br/>
        <span>调用形式：/select_smile</span><br/>
        
         成功返回值：
                {
                array[object]  //返回一个数组，每个笑话的信息为数组中的一个对象
                }
              
            }

   <h4>获得推荐话题</h4>
        <span>接口：/select_top</span><br/>
        <span>请求：get</span><br/>
        <span>参数：无调用参数</span><br/>
        <span>调用形式：/select_top</span><br/>
        
         成功返回值：
                {
                array[object]  //返回一个数组，每个话题的信息为数组中的一个对象
                }
              
            }


   <h4>查询院校库</h4>
        <span>接口：/select_school</span><br/>
        <span>请求：get</span><br/>
        <span>参数：
            sch_name 
        </span><br/>
        <span>调用形式：/select_school?sch_name='北京大学'</span><br/>
        
        成功返回值：
                {
                 array[object] 每个object为一个详细信息
                }
        错误返回值：
                    status: 1,
                    info: 'error2',
                    message: '错误'
            }



   <h4>搜索资源</h4>
        <span>接口：/select_course</span><br/>
        <span>请求：get</span><br/>
        <span>参数：
            cou_name
        </span><br/>
        <span>调用形式：/select_course?cou_name='数学一'</span><br/>
        
        成功返回值：
                {
                 array[object]  每个object为一个详细信息
                }
        错误返回值：
                status: 1,
                    info: 'error2',
                    message: '错误'
            }


      <h4>学习视频</h4>
        <span>接口：/video</span><br/>
        <span>请求：get</span><br/>
        <span>参数：无</span><br/>
          
        成功返回值：
              array[object]
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );


  <h4>考研百科</h4>
        <span>接口：/news</span><br/>
        <span>请求：get</span><br/>
        <span>参数：无</span><br/>
          
        成功返回值：
              array[object]
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );


  <h4>数学英语政治资料</h4>
        <span>接口：/learnFile</span><br/>
        <span>请求：get</span><br/>
        <span>参数：fileVerify   资料分类识别码</span><br/>
          
        成功返回值：
              array[object]
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );


  

----------------------------------------------------- 信息分享 -----------------------------------------------------------

------------------------------------------------------ 消息 ------------------------------------------------------------
 <h4>发送消息</h4>
        <span>/sendMessage</span><br/>
        <span>接口：/sendMessage</span><br/>
        <span>请求：POST</span><br/>
        <span>参数：
          stu2_id 目标用户id
          content 消息内容
          stu1_id 发送用户id 
        </span><br/>

        成功返回值：
               status:0,
                info:'ok',
                message:'成功'
              
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );
          
 <h4>接收消息</h4>
        <span>/receiveMessage</span><br/>
        <span>接口：/receiveMessage</span><br/>
        <span>请求：POST</span><br/>
        <span>参数：
          content 消息内容
          from_id 源用户id
        </span><br/>

        成功返回值：
               status:0,
                info:'ok',
                message:'成功'
              
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );

------------------------------------------------------经验贴---------------------------------------------------------------

  <h4>写贴</h4>
        <span>/writeNote</span><br/>
        <span>接口：/writeNote</span><br/>
        <span>请求：POST</span><br/>
        <span>参数：
           poster_id 学生id<br/>
            content 发帖内容<br/>
            img 图片<br/>
        </span><br/>

        成功返回值：
               status:0,
                info:'ok',
                message:'成功'
              
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );


  <h4>提问帖子</h4>
        <span>/questionNote</span><br/>
        <span>接口：/questionNote</span><br/>
        <span>请求：POST</span><br/>
        <span>参数：
           poster_id 学生id<br/>
            content 提问内容<br/>
            stu_id  提问用户id</br>
        </span><br/>

        成功返回值：
               status:0,
                info:'ok',
                message:'成功'
              
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );


  <h4>回复帖子</h4>
        <span>/answerNote</span><br/>
        <span>接口：/answerNote</span><br/>
        <span>请求：POST</span><br/>
        <span>参数：
           poster_id 学生id<br/>
            content 回复内容<br/>
            stu_id  回复用户id</br>
        </span><br/>

        成功返回值：
               status:0,
                info:'ok',
                message:'成功'
              
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );
                    


  <h4>得到所有帖子</h4>
        <span>接口：/getAllNotes</span><br/>
        <span>请求：get</span><br/>
        <span>参数：无</span><br/>
          
        成功返回值：
              array[object]
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );


  <h4>得到自己的帖子</h4>
        <span>接口：/getOwnNotes</span><br/>
        <span>请求：get</span><br/>
        <span>参数：stu_id</span><br/>
          
        成功返回值：
              array[object]
            }
        错误返回值:{
                    status:1,
                    info:'error',
                    message:'数据库错误'
            }    
            );

  
  
