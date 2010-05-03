#--------------------------------------------------------------------------
# File and Version Information:
#  $Id$
#
# Description:
#  SConscript file for package numpy
#------------------------------------------------------------------------

# Do not delete following line, it must be present in 
# SConscript file for any SIT project
Import('*')

from os.path import join as pjoin
from SConsTools.standardExternalPackage import standardExternalPackage

#
# For the standard external packages which contain includes, libraries, 
# and applications it is usually sufficient to call standardExternalPackage()
# giving some or all parameters.
#

numpy_ver = "1.3.0"
python_ver = env['PYTHON_VERSION']
PREFIX  = pjoin(env['SIT_ROOT'],"sw/external/numpy",numpy_ver)

PYDIR = "lib"
if env['SIT_ARCH_PROC'] == 'x86_64' : PYDIR = "lib64"
PYDIR += "/python"+python_ver+"/site-packages/numpy"
PYDIRSEP = True

INCDIR = PYDIR + "/core/include/numpy"

standardExternalPackage ( 'numpy', **locals() )
