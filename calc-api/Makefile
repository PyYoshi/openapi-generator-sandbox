OPENAPI_GENERATOR_VERSION=4.0.1
OPENAPI_GENERATOR_HOME=~/bin/openapitools
OPENAPI_GENERATOR_CLI=OPENAPI_GENERATOR_VERSION=${OPENAPI_GENERATOR_VERSION} ${OPENAPI_GENERATOR_HOME}/openapi-generator-cli

setup:
	mkdir -p ${OPENAPI_GENERATOR_HOME}
	curl https://raw.githubusercontent.com/OpenAPITools/openapi-generator/master/bin/utils/openapi-generator-cli.sh > ${OPENAPI_GENERATOR_HOME}/openapi-generator-cli
	chmod u+x ${OPENAPI_GENERATOR_HOME}/openapi-generator-cli
	${OPENAPI_GENERATOR_CLI} version

generate-client:
	rm -rf typescript-axios/
	mkdir -p typescript-axios/
	${OPENAPI_GENERATOR_CLI} generate -g typescript-axios -i ./openapi.yaml -c ./openapi-config.yaml -o ./typescript-axios
	cd typescript-axios && npm i && npm run build


