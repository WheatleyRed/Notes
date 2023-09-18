# 常见的通道贴图和各种贴图的意思

Diffuse/Albedo/Basecolor:漫反射/基础颜色贴图，用于模拟表面的漫反射

Reflection/Specular:反射

Metalness/Material:金属度

Glossiness:光泽度

roughnessMap:粗糙度贴图，用于模拟表面的粗糙度

normalMap:法线贴图，用于模拟表面的凹凸

Displacement/Height:置换

Bump:凹凸

Ambient Occlusion(AO):环境光遮挡贴图，用于模拟表面的环境光遮挡

alphaMap:透明度贴图，用于模拟表面的透明度

occlusionMap:遮挡贴图，用于模拟表面的遮挡

Paint：油漆，用于模拟表面的油漆

# 制作材质球
制作材质球的步骤：
1.创建材质球
2.创建贴图
3.将贴图拖入材质球
4.调整材质球的参数
制作材质球有两个重点
重点之一：材质区分
重点之二：获取AO贴图的UV channel


## 注意部分贴图的UV有两套，需要分离出来

# 贴图链接过程
Albedo与AO以颜色混合节点链接，模式为叠加相乘
接着与颜色常数（作为该层材质的底色）节点链接，模式为叠加相乘

上面这层以diffuse color输入
roughness贴图以Refl Weight输入
normal贴图以凹凸Bump输入

最后以Material贴图作为底色与上层混合输入
