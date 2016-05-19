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

assert env.get('CONDA', False), "not conda build"

pkg     = "numpy"

# link in header files
INCDIR  = pjoin('$CONDA_ENV_PATH', 'lib', '$PYTHON', 'site-packages', pkg, 'core', 'include', pkg)

standardExternalPackage(pkg, **locals())
