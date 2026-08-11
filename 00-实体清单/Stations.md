# 实体清单：Stations（28 个）

> 来源层分布: 上游 24, _Starlight 4

- `模板` **BaseStation** — `BaseStation`
- `模板` **BaseStationAlertArmories** — `BaseStationAlertArmories` ｜_Starlight
- `模板` **BaseStationAlertLevels** — `BaseStationAlertLevels`
- `模板` **BaseStationAllEventsEligible** — `BaseStationAllEventsEligible`
- `模板` **BaseStationArrivals** — `BaseStationArrivals`
- `模板` **BaseStationCargo** — `BaseStationCargo`
- `模板` **BaseStationCentcomm** — `BaseStationCentcomm`
- `模板` **BaseStationCryoTeleportation** — `BaseStationCryoTeleportation` ｜_Starlight
- `模板` **BaseStationDeliveries** — `BaseStationDeliveries`
- `模板` **BaseStationEvacuation** — `BaseStationEvacuation`
- `模板` **BaseStationExpeditions** — `BaseStationExpeditions`
- `模板` **BaseStationGateway** — `BaseStationGateway`
- `模板` **BaseStationJobsSpawning** — `BaseStationJobsSpawning`
- `模板` **BaseStationMagnet** — `BaseStationMagnet`
- `模板` **BaseStationNanotrasen** — `BaseStationNanotrasen`
- `模板` **BaseStationNews** — `BaseStationNews`
- `模板` **BaseStationRecords** — `BaseStationRecords`
- `模板` **BaseStationSalvageJobs** — `BaseStationSalvageJobs`
- `模板` **BaseStationSecureTerminal** — `BaseStationSecureTerminal` ｜_Starlight
- `模板` **BaseStationShuttles** — `BaseStationShuttles`
- `模板` **BaseStationSiliconLawCrewsimov** — `BaseStationSiliconLawCrewsimov`
- `模板` **BaseStationSyndicate** — `BaseStationSyndicate`
- **NanotrasenCentralCommand** — `NanotrasenCentralCommand` ｜父类: BaseStation,BaseStationAlertLevels,BaseStationNanotrasen,BaseStationCryoTeleportation
- **StandardNanotrasenStation** — `StandardNanotrasenStation` ｜父类: StandardNanotrasenStationTestOnly,BaseStationAlertArmories ｜_Starlight
- **StandardNanotrasenStationTestOnly** — `StandardNanotrasenStationTestOnly` ｜父类: BaseStation,BaseStationNews,BaseStationCargo,BaseStationJobsSpawning,BaseStationRecords,BaseStationArrivals,BaseStationGateway,BaseStationShuttles,BaseStationCentcomm,BaseStationEvacuation,BaseStationAlertLevels,BaseStationMagnet,BaseStationExpeditions,BaseStationSalvageJobs,BaseStationSiliconLawCrewsimov,BaseStationAllEventsEligible,BaseStationNanotrasen,BaseStationDeliveries,BaseStationCryoTeleportation,BaseStationSecureTerminal
- **StandardNukieOutpost** — `StandardNukieOutpost` ｜父类: BaseStation,BaseStationSyndicate
- **StandardStationArena** — `StandardStationArena` ｜父类: BaseStation,BaseStationJobsSpawning,BaseStationRecords,BaseStationNanotrasen
- **TestStation** — `TestStation` ｜父类: BaseStation,BaseStationJobsSpawning,BaseStationRecords,BaseStationAlertLevels
