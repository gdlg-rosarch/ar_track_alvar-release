# Script generated with Bloom
pkgdesc="ROS - This package is a ROS wrapper for Alvar, an open source AR tag tracking library."
url='http://ros.org/wiki/ar_track_alvar'

pkgname='ros-lunar-ar-track-alvar'
pkgver='0.7.1_1'
pkgrel=1
arch=('any')
license=('LGPL-2.1'
)

makedepends=('ros-lunar-ar-track-alvar-msgs'
'ros-lunar-catkin'
'ros-lunar-cmake-modules'
'ros-lunar-cv-bridge'
'ros-lunar-dynamic-reconfigure'
'ros-lunar-geometry-msgs'
'ros-lunar-image-transport'
'ros-lunar-message-generation'
'ros-lunar-pcl-conversions'
'ros-lunar-pcl-ros'
'ros-lunar-resource-retriever'
'ros-lunar-rosbag'
'ros-lunar-roscpp'
'ros-lunar-rospy'
'ros-lunar-rostest'
'ros-lunar-sensor-msgs'
'ros-lunar-std-msgs'
'ros-lunar-tf'
'ros-lunar-tf2'
'ros-lunar-visualization-msgs'
'tinyxml'
)

depends=('ros-lunar-ar-track-alvar-msgs'
'ros-lunar-cv-bridge'
'ros-lunar-dynamic-reconfigure'
'ros-lunar-geometry-msgs'
'ros-lunar-image-transport'
'ros-lunar-message-runtime'
'ros-lunar-pcl-conversions'
'ros-lunar-pcl-ros'
'ros-lunar-resource-retriever'
'ros-lunar-roscpp'
'ros-lunar-rospy'
'ros-lunar-sensor-msgs'
'ros-lunar-std-msgs'
'ros-lunar-tf'
'ros-lunar-tf2'
'ros-lunar-visualization-msgs'
'tinyxml'
)

conflicts=()
replaces=()

_dir=ar_track_alvar
source=()
md5sums=()

prepare() {
    cp -R $startdir/ar_track_alvar $srcdir/ar_track_alvar
}

build() {
  # Use ROS environment variables
  source /usr/share/ros-build-tools/clear-ros-env.sh
  [ -f /opt/ros/lunar/setup.bash ] && source /opt/ros/lunar/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/lunar \
        -DPYTHON_EXECUTABLE=/usr/bin/python2 \
        -DPYTHON_INCLUDE_DIR=/usr/include/python2.7 \
        -DPYTHON_LIBRARY=/usr/lib/libpython2.7.so \
        -DPYTHON_BASENAME=-python2.7 \
        -DSETUPTOOLS_DEB_LAYOUT=OFF
  make
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}/" install
}

