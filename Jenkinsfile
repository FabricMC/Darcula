node {
   stage 'Checkout'

   checkout scm

   stage 'Build'

   sh "rm -rf build/libs/"
   sh "chmod +x gradlew"
   sh "./gradlew build --refresh-dependencies"

   stage "Upload artifacts"

   sh "./gradlew publish"
}