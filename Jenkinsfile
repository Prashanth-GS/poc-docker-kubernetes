node {

    stage 'Cloning Repo'
        sh "git clone https://github.com/Prashanth-GS/poc-docker-kubernetes"

    stage 'Building the image'
        sh "docker build -t bnprashanth/poc-docker-kubernetes -f poc-docker-kubernetes/Dockerfile.dev ."
  
    stage 'Running the image for test'
        sh "docker run -e CI=true bnprashanth/poc-docker-kubernetes npm run test -- --coverage"
}