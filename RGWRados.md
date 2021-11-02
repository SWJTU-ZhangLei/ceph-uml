@startuml
RGWStore <|-- RGWRadosStore
RGWRadosStore o-- RGWRados
RGWRados o-- RGWRadosStore

RGWRados o-- RGWGC
RGWRados o-- RGWLC
RGWRados o-- RGWMetaNotifier
RGWRados o-- RGWDataNotifier
RGWRados o-- RGWMetaSyncProcessorThread
RGWRados o-- RGWSyncTraceManager
RGWRados o-- RGWSyncLogTrimThread
RGWRados o-- RGWServices
RGWRados o-- RGWCtl
RGWRados o-- RGWReshard

@enduml