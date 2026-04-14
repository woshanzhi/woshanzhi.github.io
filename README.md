# woshanzhi.github.io
word 插入图片，插入emf 图片可以保证放大仍是清晰

latex 则是插入eps 放大仍清晰，需要用专门的软件打开


https://zhuanlan.zhihu.com/p/531619117
画图
PlotNeuralNet



推荐好用的深度学习框架绘制工具（含教程）


3.PlotNeuralNet
4.PPT
5.Visio

3.PlotNeuralNet
亮点：脚本化，使用LaTex编写或者使用Python脚本编写结构模型，自由度高(直接网络结构代码生成可视化图，真香)。很多论文的插图就是使用这个工具可视化的。
https://github.com/HarisIqbal88/PlotNeuralNet

代码2-unet.py

  import sys
  sys.path.append('../')
  from pycore.tikzeng import *
  from pycore.blocks  import *
  
  arch = [ 
      # 开头
      to_head('..'), 
      to_cor(),
      to_begin(),
      
      #　添加输入层
      to_input( '../examples/fcn8s/cats.jpg' ),
  
      #  添加block1包含一个二重卷积接relu
      to_ConvConvRelu( name='ccr_b1', s_filer=500, n_filer=(64,64), offset="(0,0,0)", to="(0,0,0)", width=(2,2), height=40, depth=40  ),
      to_Pool(name="pool_b1", offset="(0,0,0)", to="(ccr_b1-east)", width=1, height=32, depth=32, opacity=0.5),
      #  添加三个block，每个包含三个二卷积加一池化
      *block_2ConvPool( name='b2', botton='pool_b1', top='pool_b2', s_filer=256, n_filer=128, offset="(1,0,0)", size=(32,32,3.5), opacity=0.5 ),
      *block_2ConvPool( name='b3', botton='pool_b2', top='pool_b3', s_filer=128, n_filer=256, offset="(1,0,0)", size=(25,25,4.5), opacity=0.5 ),
      *block_2ConvPool( name='b4', botton='pool_b3', top='pool_b4', s_filer=64,  n_filer=512, offset="(1,0,0)", size=(16,16,5.5), opacity=0.5 ),
  
      #  瓶颈，为block5
      to_ConvConvRelu( name='ccr_b5', s_filer=32, n_filer=(1024,1024), offset="(2,0,0)", to="(pool_b4-east)", width=(8,8), height=8, depth=8, caption="Bottleneck"  ),
      to_connection( "pool_b4", "ccr_b5"),
  
      #　解码器
      #  多个block，每个为unconv
      *block_Unconv( name="b6", botton="ccr_b5", top='end_b6', s_filer=64,  n_filer=512, offset="(2.1,0,0)", size=(16,16,5.0), opacity=0.5 ),
      to_skip( of='ccr_b4', to='ccr_res_b6', pos=1.25),
      *block_Unconv( name="b7", botton="end_b6", top='end_b7', s_filer=128, n_filer=256, offset="(2.1,0,0)", size=(25,25,4.5), opacity=0.5 ),
      to_skip( of='ccr_b3', to='ccr_res_b7', pos=1.25),    
      *block_Unconv( name="b8", botton="end_b7", top='end_b8', s_filer=256, n_filer=128, offset="(2.1,0,0)", size=(32,32,3.5), opacity=0.5 ),
      to_skip( of='ccr_b2', to='ccr_res_b8', pos=1.25),    
      
      *block_Unconv( name="b9", botton="end_b8", top='end_b9', s_filer=512, n_filer=64,  offset="(2.1,0,0)", size=(40,40,2.5), opacity=0.5 ),
      to_skip( of='ccr_b1', to='ccr_res_b9', pos=1.25),
      
      to_ConvSoftMax( name="soft1", s_filer=512, offset="(0.75,0,0)", to="(end_b9-east)", width=1, height=40, depth=40, caption="SOFT" ),
      to_connection( "end_b9", "soft1"),
      #  结束
      to_end() 
      ]
  
  def main():
      namefile = str(sys.argv[0]).split('.')[0]
      to_generate(arch, namefile + '.tex' )
  if __name__ == '__main__':
      main()
      
运行：python 2-unet.py 即可生成：


u-net网络结构
使用教程：使用PlotNeuralNet绘制深度学习网络图

4.PPT
亮点：上手快，便于操作

5.Visio
亮点：Visio更适合新手上手，绘制复杂项目的流程图和线框，因为更赞的模板；更丰富的共享组件、布局；更便利的多人协作（利用library）
