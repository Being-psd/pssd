pipeline{
		agent{
				label{
						label 'built-in'
						customWorkspace '/mnt/myproject'
					}
				}
				stages{
						stage('deploy'){
								steps{
									sh "cp -r index.html /var/www/html/"
									sh "chmod -R 777 /var/www/html"
									}
								}
						stage('stage-2'){
								steps{
									sh "systemctl start httpd"
									}
								}
					stage('stage-3'){
						steps{
							sleep 20
						}
					}
				}
}
