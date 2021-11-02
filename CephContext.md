@startuml
CephContext o-- ConfigProxy
CephContext o-- ceph::logging::Log


class ConfigValues {
    ceph::logging::SubsystemMap subsys
}
ConfigProxy o-- ConfigValues
ConfigValues o-- Option::value_t
ConfigValues o-- ceph::logging::SubsystemMap


class ObserverMgr<md_config_obs_t> {

}

ConfigProxy o-- ObserverMgr

ConfigProxy o-- md_config_t


@enduml