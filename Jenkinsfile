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
		sh 'mkdir -p Build-Release/build-Utilities-sdk3_22_F3Bv2-Release'
		sh 'ls'
		echo 'Build directories created ...'
		echo 'Copying pro files ...'
		sh 'cp ProFiles-Jenkins/Utilities.pro Utilities'
		sh 'cp ProFiles-Jenkins/SecurityFramework.pro SecurityFramework'
		sh 'cp ProFiles-Jenkins/InputParameterFramework.pro InputParameterFramework'
		sh 'cp ProFiles-Jenkins/OutputFramework.pro OutputFramework'
		sh 'cp ProFiles-Jenkins/CardFramework.pro CardFramework'
		sh 'cp ProFiles-Jenkins/TicketReader.pro TicketReader'
		echo 'Pro files copied ...'
            }
        }
        stage('Build-Utilities') {
            steps {
		echo 'Building Utilities ...'
                sh 'pwd'
		sh 'source /home/$USER/aep/sdk-3.22/toolchain-F3Bv2/environment-setup-cortexa9hf-neon-poky-linux-gnueabi'
		sh 'cd ./Build-Release/build-Utilities-sdk3_22_F3Bv2-Release'
		sh 'pwd'
		sh '/home/$USER/aep/sdk-3.22/toolchain-F3Bv2/sysroots/i686-pokysdk-linux/usr/bin/qt5/qmake ../../Utilities/Utilities.pro -spec f3bv2-aep-cortexa9-g++'
		sh '/usr/bin/make'
		sh 'cp libUtilities.so libUtilities.so.1 libUtilities.so.1.0 libUtilities.so.1.0.0 ../../bin'
		sh 'cp libUtilities.so libUtilities.so.1 libUtilities.so.1.0 libUtilities.so.1.0.0 ../../Libs'
		sh 'cd ../..'
		sh 'pwd'
		echo 'Finished building Utilities ...'
            }
        }
        stage('Build-SecurityFramework') {
            steps {
		echo 'Building SecurityFramework ...'
                sh 'pwd'
		sh 'source /home/$USER/aep/sdk-3.22/toolchain-F3Bv2/environment-setup-cortexa9hf-neon-poky-linux-gnueabi'
		sh 'cd ./Build-Release/build-SecurityFramework-sdk3_22_F3Bv2-Release'
		sh 'pwd'
		sh '/home/$USER/aep/sdk-3.22/toolchain-F3Bv2/sysroots/i686-pokysdk-linux/usr/bin/qt5/qmake ../../SecurityFramework/SecurityFramework.pro -spec f3bv2-aep-cortexa9-g++'
		sh '/usr/bin/make'
		sh 'cp libSecurityFramework.so libSecurityFramework.so.1 libSecurityFramework.so.1.0 libSecurityFramework.so.1.0.0 ../../bin'
		sh 'cp libSecurityFramework.so libSecurityFramework.so.1 libSecurityFramework.so.1.0 libSecurityFramework.so.1.0.0 ../../Libs'
		sh 'cd ../..'
		sh 'pwd'
		echo 'Finished building SecurityFramework ...'
            }
        }
        stage('Build-InputParameterFramework') {
            steps {
		echo 'Building InputParameterFramework ...'
                sh 'pwd'
		sh 'source /home/$USER/aep/sdk-3.22/toolchain-F3Bv2/environment-setup-cortexa9hf-neon-poky-linux-gnueabi'
		sh 'cd ./Build-Release/build-InputParameterFramework-sdk3_22_F3Bv2-Release'
		sh 'pwd'
		sh '/home/$USER/aep/sdk-3.22/toolchain-F3Bv2/sysroots/i686-pokysdk-linux/usr/bin/qt5/qmake ../../InputParameterFramework/InputParameterFramework.pro -spec f3bv2-aep-cortexa9-g++'
		sh '/usr/bin/make'
		sh 'cp libInputParameterFramework.so libInputParameterFramework.so.1 libInputParameterFramework.so.1.0 libInputParameterFramework.so.1.0.0 ../../bin'
		sh 'cp libInputParameterFramework.so libInputParameterFramework.so.1 libInputParameterFramework.so.1.0 libInputParameterFramework.so.1.0.0 ../../Libs'
		sh 'cd ../..'
		sh 'pwd'
		echo 'Finished building InputParameterFramework ...'
            }
        }
        stage('Build-OutputFramework') {
            steps {
		echo 'Building OutputFramework ...'
                sh 'pwd'
		sh 'source /home/$USER/aep/sdk-3.22/toolchain-F3Bv2/environment-setup-cortexa9hf-neon-poky-linux-gnueabi'
		sh 'cd ./Build-Release/build-OutputFramework-sdk3_22_F3Bv2-Release'
		sh 'pwd'
		sh '/home/$USER/aep/sdk-3.22/toolchain-F3Bv2/sysroots/i686-pokysdk-linux/usr/bin/qt5/qmake ../../OutputFramework/OutputFramework.pro -spec f3bv2-aep-cortexa9-g++'
		sh '/usr/bin/make'
		sh 'cp libOutputFramework.so libOutputFramework.so.1 libOutputFramework.so.1.0 libOutputFramework.so.1.0.0 ../../bin'
		sh 'cp libOutputFramework.so libOutputFramework.so.1 libOutputFramework.so.1.0 libOutputFramework.so.1.0.0 ../../Libs'
		sh 'cd ../..'
		sh 'pwd'
		echo 'Finished building OutputFramework ...'
            }
        }
        stage('Build-CardFramework') {
            steps {
		echo 'Building CardFramework ...'
                sh 'pwd'
		sh 'source /home/$USER/aep/sdk-3.22/toolchain-F3Bv2/environment-setup-cortexa9hf-neon-poky-linux-gnueabi'
		sh 'cd ./Build-Release/build-CardFramework-sdk3_22_F3Bv2-Release'
		sh 'pwd'
		sh '/home/$USER/aep/sdk-3.22/toolchain-F3Bv2/sysroots/i686-pokysdk-linux/usr/bin/qt5/qmake ../../CardFramework/CardFramework.pro -spec f3bv2-aep-cortexa9-g++'
		sh '/usr/bin/make'
		sh 'cp libCardFramework.so libCardFramework.so.1 libCardFramework.so.1.0 libCardFramework.so.1.0.0 ../../bin'
		sh 'cp libCardFramework.so libCardFramework.so.1 libCardFramework.so.1.0 libCardFramework.so.1.0.0 ../../Libs'
		sh 'cd ../..'
		sh 'pwd'
		echo 'Finished building CardFramework ...'
            }
        }
        stage('Build-TicketReader') {
            steps {
		echo 'Building TicketReader ...'
                sh 'pwd'
		sh 'source /home/$USER/aep/sdk-3.22/toolchain-F3Bv2/environment-setup-cortexa9hf-neon-poky-linux-gnueabi'
		sh 'cd ./Build-Release/build-TicketReader-sdk3_22_F3Bv2-Release'
		sh 'pwd'
		sh '/home/$USER/aep/sdk-3.22/toolchain-F3Bv2/sysroots/i686-pokysdk-linux/usr/bin/qt5/qmake ../../TicketReader/TicketReader.pro -spec f3bv2-aep-cortexa9-g++'
		sh '/usr/bin/make'
		sh 'cp TicketReader ../../bin'
		sh 'cd ../..'
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
