node('docker') {
 
    stage 'Checkout'
        checkout scm
    stage 'Building the image'
        sh "docker build -t bnprashanth/poc-docker-kubernetes -f Dockerfile.dev ."
  
    stage 'Running the image for test'
        sh "docker run -e CI=true bnprashanth/poc-docker-kubernetes npm run test -- --coverage"
}