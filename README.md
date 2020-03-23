# temizlik_robotu

TEMIZLIK ROBOTU




Workspace yok ise workspace oluşturunuz.

Örn. http://wiki.ros.org/catkin/Tutorials/create_a_workspace

Daha sonra workspace gidiniz ve paketi indiriniz.

cd ~/<WORKSPACE_NAME>/src

git clone "https://github.com/inomuh/temizlik_robotu.git"


cd ~/<WORKSPACE_NAME>

catkin_make

catkin_make install

source devel/setup.bash

$ roslaunch temizlik_robotu_baslat temizlik_robotu_baslat.launch

Görev tamamlama yüzdesini görmek için

$ rosrun temizlik_robotu temizlik_robotu_bilgi_servisi_baslat.launch
