pipeline {
    agent any

    stages {
        stage('Setup') {
            steps {
                echo 'Performing pre build steps ...'
		echo 'Creating build directories ...'
                sh 'pwd'
		sh 'mkdir Libs'
		sh 'mkdir bin'
		sh 'mkdir -p Build-Release/build-TicketReader-sdk3_22_F3Bv2-Release'
		sh 'ls'
		echo 'Build directories created ...'
            }
        }
        stage('Build-TicketReader') {
            steps {
		echo 'Building TicketReader ...'
                sh 'pwd'
		sh 'source /home/$USER/aep/sdk-3.22/toolchain-F3Bv2/environment-setup-cortexa9hf-neon-poky-linux-gnueabi'
		dir('Build-Release/build-TicketReader-sdk3_22_F3Bv2-Release') {
                    sh 'pwd'
		    sh '/home/$USER/aep/sdk-3.22/toolchain-F3Bv2/sysroots/i686-pokysdk-linux/usr/bin/qt5/qmake ../../Utilities/TestJenkins.pro -spec f3bv2-aep-cortexa9-g++'
		    sh '/usr/bin/make'
		    sh 'cp TestJenkins ../../bin'
                }
		sh 'pwd'
		echo 'Finished building TicketReader ...'
            }
        }
        stage('Build-Artifacts') {
            steps {
		echo 'Copying Build-Artifacts ...'
                sh 'pwd'
		sh 'cp -r bin /home/$USER/Downloads/bin-$(date +%d-%m-%y-%H:%M:%S)'
		sh 'pwd'
		echo 'Finished copying artifacts ...'
            }
        }
        stage('CleanUp') {
            steps {
		echo 'Starting cleanup ...'
                sh 'pwd'
		echo 'TODO...'
            }
        }
    }
}
