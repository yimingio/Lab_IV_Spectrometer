在这一部分，我们将讨论spectrometer的设计。

根据实验一，我们确定，DVD具有更强的diffraction diserpasion ，即对不同波长的光，DVD能将他们分散的更开，这将有助于提高spectrometer的精度。因此在spectrometer中，我们采用DVD作为光栅。

在spectrometer中，我们使用一个720p的相机模组作为采集数据的终端，我们去除了相机上的红外线滤镜，以减少对长波长可见光的透射率，提高实验的准确性。同时该相机使用手动对焦，在黑暗的spectrometer内部避免了自动对焦带来的模糊，由于使用距离一般不会发生变化，手动对焦具有更高的稳定性和精确度，

相机模组与DVD光栅被紧贴在一起，以保证相机能够拍摄到清晰的衍射条纹。二者被垂直安放在腔体内，与一个可以旋转的硬纸板平台，方便我们调整相机的指向，以使得能在相机中拍摄到清晰准确的衍射条纹。

首先我们根据NNIN的DIY实验指南，在一个纸盒中制作了spectrometer的原型机如图。这里我们使用纸板制作了一条狭缝，使得光线能够尽可能的保持垂直入射。

光线通过狭缝将通过倾斜的光栅上，不同颜色的光线将被衍射到不同的角度并最终被相机模组的传感器记录。得到如下的条纹。

在软件上，我们使用由（）创作的python程序，他通过测量相机中心水平线上各个位置的光线亮度得到一条发光强度光谱，如图，使用红色激光与绿色激光进行校准后，每个点位一一对应入射光的不同的波长。最终我们将得到一个入射光的光强度光谱数据集。

值得注意的是，得到的光强度光谱是根据最亮点作为100%进行计算的相对值，因此在之后的数据分析过程中，我们需要更改数据分析的流程，这将在之后的介绍中进行展现。

在进行了原型机的测试之后，我们发现这一原理进行实验具有可行性，同时我们可以得到若干我们需要的关键数据：

* 狭缝的长度与宽度
* 相机与滤镜组与入射光线之间的夹角
* 相机与狭缝之间的相对位置。

因此我们使用这些数据可以绘制我们正式的spectrometer的3D图纸。

Spectrometer将被分做若干个不同的部分，通过拼装我们可以对仪器进行灵活的调整。

* Mainbody
* Spectrometer cover
* Camera dock
* Disc dock.

## Mainbody

mainbody是spectrometer的主要部分，其构成了spectrometer的腔体，并在上面有与各个部件的连接部位。spectrometer的头是一个突出的圆形环，用于与测试模组进行连接，突出的部分剪保证在连接处不会有环境光的干扰。圆形环中间是一条狭缝，狭缝过滤掉倾斜入射的光。

mainbody的后端有一个药丸形状的Mounting slot，这将与camera dock 的底座相固定，同时允许相机进行左右移动与旋转，调节入射光谱在相机中的成像位置。

Mainbody的上端与前端分别预留了一组用于与其他部分的进行连接的magnetic ports，在本次设计中，我们使用磁铁对各个部分进行连接。既保证了一定的连接稳定强度，同时有助于拆装调整。

## Spectrometer cover

Spectrometer cover与mainbody相连接构成了一个spectrometer的封闭腔体，防止环境光对内部传感器的影响，与mainbody一样，cover具有固定camera dock的mounting slot，和magnetic port，用于与mainbody进行固定，cover的四周向外延伸，使得环境光无法通过缝隙进入。

## Camera Dock

Camera dock由上下两个圆形底座与中间固定板构成。中间的固定板上预留了用于塞入相机模组的空隙以及螺丝孔位，以及用于与disc dock进行连接的固定方形柱。

## Disc Dock

DIsc dock 有三个不同形状的开孔，两侧为与comera dock进行连接的方形空洞，中心为用于固定光栅的狭缝。disc dock在安装在camera dock上之后，仍然具有前后移动的活动性。以适应手动变焦过程中镜头的伸缩。

## Others

所有实验部件使用白色树脂3D打印，存在一定的透光性，为了避免环境光的影响。所有的另加内部都被遮光胶布进行覆盖，使得光线无法透过。







## Testing Module

在本次使用中我们将进行两个使用spectrometer的应用，分别对应实验2和试验3，因此在一下部分将分别介绍

## LED Module

LED模组比较简单，其上面有两条导轨，这两条导轨与迷你面包版的反面的螺丝孔位相对应，可以将LED等固定在于狭缝同一直线的位置，是的LED释放的光线能够垂直进入spectrometer。

实验使用了了串联的方式将多个LED灯珠进行相连，这种方法既提高了实验的亮度，同时拉大了不同颜色的LED灯的正向电压之间的差距，有利于电压表测量时产生的误差。Module的侧壁有一个空位用于连接内外不的电路，电压表可以通过测量留在外部的端口对内部的LED正向电压进行测量。

## Cuvette Module

Cuvette Module由前盖，后板，以及中间的cuvette shelf构成，前盖上具有与spectrometer进行连接的端口，而后盖则安装有照明电路与白色LED灯板，用于提供光。中间的cuvette shelf可以同时固定5个cuvette以进行测量，可以通过滑动平移两侧的杆子调整spectrometer测量的cuvette实现在不拆开的条件下对多个实验的侧了，能够大大提高效率。

此处使用白色LED灯板提供光线，白色LED灯板能均匀稳定的蓝色与红色光，这将有助于在实验3中对吸收率进行的探究。









