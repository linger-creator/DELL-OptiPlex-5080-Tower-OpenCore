# DELL-OptiPlex-5080-Tower-OpenCore

- OptiPlex 5080 Tower Hackintosh OpenCore MacOS 15 Sequoia

### OS Version Tested

- MacOS  Sequoia 15.7.3

# 

### Hardware

- Motherboard: DELL Q470

- Bios Version:

- CPU: Intel i5 10500

- RAM: Samsung 1x8GB DDR4 3200

- SSD:YSR01TBHLCA1-E5C-2 Media

- iGPU: Intel UHD Graphic 630

- Audio:Realtek ALC256(ALC3246)

- Ethernet Card: Intel I219-LM


### Bios Setup



 | Name | Option |

 | ----- | --- |

 | System Configuration → SATA Operation | AHCI |

 | Security → PTT Security/PTT On | Disabled |

 | Secure Boot → Secure Boot Enable | Disabled |

 | PSecure Boot → Secure Boot Mode | Audit Mode |

 | Intel Software Guard Extensions → Intel SGX Enable | Disabled |

 | Power Management → Deep Sleep Control | Disabled |

 | Power Management → USB Wake Support | Disabled |

 | Power Management → Wake on LAN/WLAN | Lan only |

 | Power Management → Block Sleep | Disabled |

 | POST Behavior → Fastboot | Minimal |

 | Virtualization Support → VT For Direct I/O | Disabled |


### Notes

  - Use [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) build your own SMBIOS

 

  - Use [RU.efi](http://ruexe.blogspot.com/) Unlock CFG LOCK , Change DVMT = 64MB



 | Option | UEFI Variable Name | Address | Default | Replace |

 | --- | --- | --- | --- | --- |

 | CFG LOCK | CPUSetup | 0x3E | 0x1 | 0x0 |

 | DVMT | SaSetup | 0xF5 | 0x0 | 0x2 |

 

- Unlock CFG LOCK Address:0x3E  01 (Enabled) Replace 00（Disabled）

 ![image](ScreenShot/RU/cpusetup.png)

 

- Change DVMT Address:0xF5  00（Default） Replace 02（64MB）

 ![image](ScreenShot/RU/sasetup.png)



### 参考配置

- https://github.com/hackintosh-club/DELL-3090MFF-OpenCore
