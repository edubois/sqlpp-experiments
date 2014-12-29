Import( 'project' )
Import( 'libs' )


SqlppExperimentsFlags = { 'LIBPATH': [project.inOutputLib()],
                'CCFLAGS': [project.CC['warning3'],project.CC['sharedobject'] ],
                'CXXFLAGS':[],
                'CPPDEFINES':[],
             }

if project.env['mode'] == 'production' :
	SqlppExperimentsFlags['CPPDEFINES'].append( 'FACTIZ_PRODUCTION' )
	if 'visibilityhidden' in project.CC:
		SqlppExperimentsFlags['SHCCFLAGS'] = [project.CC['visibilityhidden']]

# If your compiler as a flag to mark undefined flags as error in shared libraries
if 'sharedNoUndefined' in project.CC:
	SqlppExperimentsFlags['SHLINKFLAGS'] = [project.CC['sharedNoUndefined']]

SConscript( [
              'libraries/dbEngine/SConscript',
            ]
            +
            project.scanFiles( ['applications'], accept=['SConscript'] )
          )

