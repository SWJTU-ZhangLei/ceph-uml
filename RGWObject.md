@startuml
RGWStore <|-- RGWRadosStore
RGWRadosStore o-- RGWRados
RGWRados o-- RGWRadosStore

RGWRados o-- RGWGC
RGWRados o-- RGWLC
RGWRados o-- RGWMetaNotifier
RGWRados o-- RGWDataNotifier

RGWUser o-- RGWUserInfo

RGWBucket o-- RGWBucketEnt
RGWBucket o-- RGWBucketInfo
RGWBucket o-- RGWUser

RGWObject o-- RGWBucket
@enduml