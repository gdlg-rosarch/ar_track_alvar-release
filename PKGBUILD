# Script generated with Bloom
pkgdesc="ROS - This package is a ROS wrapper for Alvar, an open source AR tag tracking library."
url='http://ros.org/wiki/ar_track_alvar'

pkgname='ros-kinetic-ar-track-alvar'
pkgver='0.7.1_1'
pkgrel=1
arch=('any')
license=('LGPL-2.1'
)

makedepends=('ros-kinetic-ar-track-alvar-msgs'
'ros-kinetic-catkin'
'ros-kinetic-cmake-modules'
'ros-kinetic-cv-bridge'
'ros-kinetic-dynamic-reconfigure'
'ros-kinetic-geometry-msgs'
'ros-kinetic-image-transport'
'ros-kinetic-message-generation'
'ros-kinetic-pcl-conversions'
'ros-kinetic-pcl-ros'
'ros-kinetic-resource-retriever'
'ros-kinetic-rosbag'
'ros-kinetic-roscpp'
'ros-kinetic-rospy'
'ros-kinetic-rostest'
'ros-kinetic-sensor-msgs'
'ros-kinetic-std-msgs'
'ros-kinetic-tf'
'ros-kinetic-tf2'
'ros-kinetic-visualization-msgs'
'tinyxml'
)

depends=('ros-kinetic-ar-track-alvar-msgs'
'ros-kinetic-cv-bridge'
'ros-kinetic-dynamic-reconfigure'
'ros-kinetic-geometry-msgs'
'ros-kinetic-image-transport'
'ros-kinetic-message-runtime'
'ros-kinetic-pcl-conversions'
'ros-kinetic-pcl-ros'
'ros-kinetic-resource-retriever'
'ros-kinetic-roscpp'
'ros-kinetic-rospy'
'ros-kinetic-sensor-msgs'
'ros-kinetic-std-msgs'
'ros-kinetic-tf'
'ros-kinetic-tf2'
'ros-kinetic-visualization-msgs'
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
  [ -f /opt/ros/kinetic/setup.bash ] && source /opt/ros/kinetic/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/kinetic \
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

