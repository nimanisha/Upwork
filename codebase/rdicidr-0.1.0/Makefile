appname = fsl

account = petenka150
stage = prod
include configs/$(stage)


build:
	docker build -t $(account)/$(appname):$(version) .

# login:
# 	aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin $(account).dkr.ecr.us-east-1.amazonaws.com

push: build
	docker push $(account)/$(appname):$(version)


deploy: push
	helm upgrade --install $(appname) k8s-chart/ --namespace=$(namespace) --create-namespace \
		--set applicationName=$(appname) \
		--set replicaCount=$(replicas) \
		--set hostname=$(hostname)
		--set image.repository=$(account)/$(appname) \
		--set image.tag=$(version)

