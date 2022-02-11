# Configure collector and Jaeger with docker

git clone git@github.com:open-telemetry/opentelemetry-ruby.git; \
    cd opentelemetry-ruby/examples/otel-collector; \
       docker-compose up -d

# configure endpoint as ENV variable
export OTEL_EXPORTER_OTLP_ENDPOINT=http://0.0.0.0:4318

# run app
go run . 

# Navigate to localhost:3232/hello-instrumented

Find traces at http://localhost:16686/
