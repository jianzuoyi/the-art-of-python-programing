# the-art-of-python-programing

python setup.py install     安装成熟包
python setup.py develop     安装开发中的包，在安装路径下面创建包的引用，适合开发的时候
pip uninstall 删除包



对语言的选择其实也是程序员对自我的定位：
是想做科学家，还是工程师。

"Python能够将一个已经证明成熟和可靠的算法实现出来，并且投入工程应用，开发出实用的决策系统。"说的很好。个人感觉用Python不是去验证一个模型的最佳选择

十分赞同阁下的这句话：“使用R，能够将工作者从习惯的算法中解脱出来，真正去思考模型本身的数学意义，在数学层面去修改算法。忘记我们经常思考的算法复杂度和内存消耗之类的问题，推动机器学习和数据挖掘的关键动力，就是数学模型！”

类、模块、包，是处理功能复用和功能颗粒度的划分
类，封闭数据
模块，对应于文件, file.py文件名去掉.py为包的名字
包，对应于文件夹，需要包含 __init__.py

引用模块或包
import 模块/包     用点标记符访问
from 模块/包 import function/*     直接访问

from Biopython:
is None, is not None

if seq is None

if id is not None

in, not in

unittest:
python -m unites discover 自动发现目录内的unit test并执行


repr, str

在可能发生异常的地方使用  
try


调试，debug
1. python中的异常栈跟踪
          import traceback
          traceback.print_exc()
sys.exc_info()
traceback.extract_tb()
     
2. 使用cgitb来简化异常调试
          cgitb.enable(format=“text”)
          不适合线上环境，适合在开发过程中使用
3. 使用logging模块来记录异常
        logging.exception(ex)
        logging.error(ex, exc_info=1)
        logging.critical(ex, exc_info=1)
     
好处：可以指定记录信息的级别，可以放心地输出不同级别的信息，也不用删除，
最后统一控制输出哪个级别的信息


try:
except:
else:


模块中，函数没有先后顺序，可以把模块专属的函数放在最后，前面的函数一样可以调用

多研究开源的优秀代码，自己少走不少弯路


2to3     python2代码转3

安全，编译部分绑定机器码


用文件、数据库存储数据，一个项目界面并不是必须的
不过是设置数据的一个接口而已，项目优先考虑不要界面的，可以快速开发
有界面，很多时间花在界面上了，不能专注于功能的实现
做成命令行，linux、mac、window都能跑，做成了界面，就限制了平台 

enumerate
当循环需要返回索引号是使用enumerate，比用循环变量方便
for (index, feature) in enumerate(gb_record.features) :

