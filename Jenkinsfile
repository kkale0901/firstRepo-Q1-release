pipeline{

agent{

label{
label "built-in"
customWorkspace "/mnt/newproject"
}
}

stages{
stage("clone_project"){

steps{
sh "rm -rf firstRepo-Q1-release/index.html /var/www/html*"
sh "git clone https://github.com/kkale0901/firstRepo-Q1-release.git"
}
}

stage("deploy_index"){

steps{
sh "cd /var/www/html"
sh"rm -rf index.html"
sh "cp /mnt/newproject/firstRepo-Q1-release/index.html /var/www/html"
sh "chmod -R 777 /var/www/html"
}
}

}

}
