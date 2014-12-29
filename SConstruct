EnsureSConsVersion( 1, 2 )
EnsurePythonVersion( 2, 5 )

import os
import sys

sys.path.append('tools')
from sconsProject import SConsProject

class SqlppExperimentsProject( SConsProject ):
    pass

#______________________________________________________________________________#

project = SqlppExperimentsProject()


Export('project')
Export({'libs':project.libs})

#______________________________________________________________________________#

project.begin()
project.SConscript()
project.end()



