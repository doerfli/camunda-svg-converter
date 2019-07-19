# Camunda BPMN to SVG converter

Docker container that includes all dependencies to convert a Camunda BPMN file to SVG via the bpmn-to-image tool.

## How to build the container

Syntax to build the container

```
docker build -t camunda-svg-converter:latest .
```

## How to run the container

```
docker run -v <directory-with-xml>:/app camunda-svg-converter bpmn-to-image <input-file>:<output-file>
```

Example to convert `diagram_1.xml` to `diagram_1.svg`

```
docker run -v /tmp/test:/app camunda-svg-converter bpmn-to-image diagram_1.xml:diagram_1.svg
```
