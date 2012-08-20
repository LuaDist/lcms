# Copyright (C) 2007-2012 LuaDist.
# Created by Peter Drahoš
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.

project ( lcms )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )

# LCMS Library
include_directories ( include )
file ( GLOB LCMS_SRCS "src/*.c" "src/*.def" )
add_library ( lcms ${LCMS_SRCS} )

# install
install_library ( lcms )
install_header ( include/icc34.h include/lcms.h )
install_doc ( doc/ )
install_data ( AUTHORS COPYING ChangeLog NEWS README.1ST )
