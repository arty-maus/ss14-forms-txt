# Access Levels Reference

Pulled from `Resources/Prototypes/Access/*.yml`, `Resources/Prototypes/Roles/Jobs/**`, and locale files in the [space-station-14](https://github.com/arty-maus/space-station-14) game source. Not in-character — dev reference for building/updating HoP forms (access requests, ID enrollment, etc.).

## Access Levels

| Access Level ID | Display Name | Source File | Notes |
|---|---|---|---|
| Command | Command | command.yml | |
| Captain | Captain | command.yml | |
| HeadOfPersonnel | Head of Personnel | command.yml | |
| EmergencyShuttleRepealAll | E.Shuttle Repeal All | command.yml | not addable to ID card |
| Cryogenics | Cryogenics | command.yml | |
| HeadOfSecurity | Head of Security | security.yml | |
| Security | Security | security.yml | |
| Armory | Armory | security.yml | |
| Brig | Brig | security.yml | |
| Detective | Detective | security.yml | |
| GenpopEnter | Enter Genpop | security.yml | |
| GenpopLeave | Leave Genpop | security.yml | |
| ChiefEngineer | Chief Engineer | engineering.yml | |
| Engineering | Engineering | engineering.yml | |
| Atmospherics | Atmospherics | engineering.yml | |
| ResearchDirector | Research Director | research.yml | |
| Research | Research | research.yml | |
| ChiefMedicalOfficer | Chief Medical Officer | medical.yml | |
| Medical | Medical | medical.yml | |
| Chemistry | Chemistry | medical.yml | |
| Paramedic | Paramedic | medical.yml | unused — no accessGroup or job references it |
| Quartermaster | Quartermaster | cargo.yml | |
| Cargo | Cargo | cargo.yml | |
| Salvage | Salvage | cargo.yml | |
| Bar | Bar | service.yml | |
| Kitchen | Kitchen | service.yml | |
| Hydroponics | Hydroponics | service.yml | |
| Service | Service | service.yml | |
| Janitor | Janitor | service.yml | |
| Theatre | Theatre | service.yml | |
| Chapel | Chapel | service.yml | |
| Lawyer | Lawyer | service.yml | |
| Maintenance | Maintenance | maintenance.yml | |
| External | External | external.yml | |
| NuclearOperative | Nuclear Operative | syndicate.yml | |
| SyndicateAgent | Syndicate Agent | syndicate.yml | |
| CentralCommand | Central Command | centcomm.yml | |
| Wizard | Wizard | wizard.yml | |
| StationAi | Artificial Intelligence | silicon.yml | not addable to ID card |
| Borg | Cyborg | silicon.yml | not addable to ID card |
| BasicSilicon | Robot | silicon.yml | not addable to ID card |
| Xenoborg | Xenoborg | xenoborg.yml | not addable to ID card |

## Access Groups (bundles)

| Access Group ID | Access Levels Included |
|---|---|
| Cargo | Quartermaster, Salvage, Cargo |
| Command | Captain, Command, ChiefEngineer, ChiefMedicalOfficer, Cryogenics, HeadOfPersonnel, HeadOfSecurity, Quartermaster, ResearchDirector |
| Engineering | ChiefEngineer, Engineering, Atmospherics |
| Medical | ChiefMedicalOfficer, Medical, Chemistry |
| Research | ResearchDirector, Research |
| Security | HeadOfSecurity, Security, Armory, Brig, Detective, Cryogenics |
| Armory | Security, Armory, Brig |
| Service | HeadOfPersonnel, Bar, Kitchen, Hydroponics, Service, Janitor, Theatre, Chapel, Lawyer |
| Silicon | StationAi, Borg, BasicSilicon |
| General | Maintenance |
| AllAccess | EmergencyShuttleRepealAll, Captain, HeadOfPersonnel, ChiefEngineer, ChiefMedicalOfficer, HeadOfSecurity, ResearchDirector, Command, Cryogenics, Security, Detective, Armory, Brig, Lawyer, Engineering, Medical, Quartermaster, Salvage, Cargo, Research, Service, Maintenance, External, Janitor, Theatre, Bar, Chemistry, Kitchen, Chapel, Hydroponics, Atmospherics, GenpopEnter, GenpopLeave |

## Jobs — Default Access

`Extended` = `extendedAccess:` field — only granted via job-swap/chameleon outfit, not issued by default.

### Civilian
| Job | Access | Extended |
|---|---|---|
| Passenger | Maintenance | — |
| Bartender | Service, Maintenance, Bar | Kitchen, Hydroponics |
| Botanist | Service, Maintenance, Hydroponics | Kitchen, Bar |
| Chaplain | Chapel, Maintenance | — |
| Chef | Service, Maintenance, Kitchen | Hydroponics, Bar |
| Clown | Theatre, Maintenance | — |
| Janitor | Service, Janitor, Maintenance | — |
| Lawyer | Service, Lawyer, Brig, Maintenance | — |
| Librarian | Service, Maintenance | — |
| Mime | Theatre, Maintenance | — |
| Musician | Maintenance, Theatre | — |
| Service Worker | Service, Maintenance, Bar, Kitchen | Hydroponics |
| Visitor | Maintenance | External |

### Command
| Job | Access |
|---|---|
| Captain | *(none listed)* — `accessGroups: [AllAccess]` |
| Head of Personnel | Command, HeadOfPersonnel, Bar, Service, Maintenance, Janitor, Theatre, Kitchen, Chapel, Hydroponics, External, Cryogenics, Chemistry, Engineering, Research, Detective, Salvage, Security, Brig, Lawyer, Cargo, Atmospherics, Medical, GenpopEnter, GenpopLeave |
| Chief Engineer | Maintenance, Engineering, Command, External, ChiefEngineer, Atmospherics, Brig, Cryogenics |
| Chief Medical Officer | Medical, Command, Maintenance, Chemistry, ChiefMedicalOfficer, Brig, Cryogenics |
| Head of Security | HeadOfSecurity, Command, Brig, Security, Armory, Maintenance, External, Detective, Cryogenics, GenpopEnter, GenpopLeave |
| Research Director | Research, Command, Maintenance, ResearchDirector, Brig, Cryogenics |
| Quartermaster | Cargo, Salvage, Quartermaster, Maintenance, External, Command, Brig, Cryogenics |

### Engineering
| Job | Access | Extended |
|---|---|---|
| Atmospheric Technician | Maintenance, Engineering, External, Atmospherics | — |
| Chief Engineer | *(see Command)* | — |
| Station Engineer | Maintenance, Engineering, External | Atmospherics |
| Technical Assistant | Maintenance, Engineering, External | Atmospherics |

### Medical
| Job | Access | Extended |
|---|---|---|
| Chemist | Medical, Chemistry, Maintenance | — |
| Chief Medical Officer | *(see Command)* | — |
| Medical Doctor | Medical, Maintenance | Chemistry |
| Medical Intern | Medical, Maintenance | — |
| Paramedic | Medical, Maintenance | Chemistry |

### Security
| Job | Access |
|---|---|
| Head of Security | *(see Command)* |
| Security Cadet | Security, Brig, Maintenance, External, Cryogenics |
| Security Officer | Security, Brig, Maintenance, External, Cryogenics |
| Detective | Security, Brig, Maintenance, Detective, Cryogenics, External |
| Warden | Security, Brig, Armory, Maintenance, External, Detective, Cryogenics, GenpopEnter, GenpopLeave |

### Science
| Job | Access |
|---|---|
| Research Director | *(see Command)* |
| Scientist | Research, Maintenance |
| Research Assistant | Research, Maintenance |

### Cargo
| Job | Access | Extended |
|---|---|---|
| Cargo Technician | Cargo, Maintenance | Salvage |
| Quartermaster | *(see Command)* | — |
| Salvage Specialist | Cargo, Salvage, Maintenance, External | — |

### Silicon
| Job | Access |
|---|---|
| Cyborg | none in job proto — granted at entity/component level |
| Station AI | none in job proto — granted at entity/component level |

### CentComm / ERT (all also carry `accessGroups: [AllAccess]`)
| Job | Access |
|---|---|
| CentComm Official | CentralCommand |
| CentComm Quarantine Officer (CBURN) | CentralCommand |
| ERT Leader | CentralCommand |
| ERT Chaplain | CentralCommand |
| ERT Engineer | CentralCommand |
| ERT Security | CentralCommand |
| ERT Medic | CentralCommand |
| ERT Janitor | CentralCommand |
| Death Squad | CentralCommand |

### Specific (misc/wildcard roles)
| Job | Access | Extended |
|---|---|---|
| Reporter | Service, Maintenance | — |
| Psychologist | Medical, Maintenance | Chemistry |

## Notes

- **Captain** has no explicit access list — grants the full `AllAccess` group instead.
- **Head of Personnel** is the broadest non-Captain access holder; effectively everything except Armory-tier security and CentComm.
- **Borg / Station AI** get silicon access (StationAi/Borg/BasicSilicon levels) from the entity, not the job prototype.
- `extendedAccess:` is chameleon/job-swap only — do not treat as default-issued when filling out forms.
- CentComm/ERT roles dual-list under both Command and CentralCommand departments in `departments.yml`.
