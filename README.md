# clusterfailover

NOMES SERVIDORES:  
HOST1CLT2  
HOST2CLT2

RODAR COMANDOS:

Install-WindowsFeature -Name Hyper-V-Tools -IncludeAllSubFeature  
Install-WindowsFeature -Name RSAT-Hyper-V-Tools -IncludeAllSubFeature  
  
instalar role de failovercluster  
instalar iscsi  
instalar mpio  
instalar dsminstaller  
  
  
New-VMSwitch -Name ADM -NetAdapterName ADM1,ADM2 -EnableEmbeddedTeaming $true  
  
New-VMSwitch -Name CLT -NetAdapterName CLT1,CLT2 -EnableEmbeddedTeaming $true  
  
New-VMSwitch -Name WAN_PENSOU -NetAdapterName WAN_PENSOU1,WAN_PENSOU2 -EnableEmbeddedTeaming $true  
  
New-VMSwitch -Name WAN_SERRASUL -NetAdapterName WAN_SRS1,WAN_SRS2 -EnableEmbeddedTeaming $true



ETIQUESTAS DAS INTERFACES
ADM1
ADM2
CLT1
CLT1
SRS1
SRS2
PNS1
PNS2
STR1
STR2
LM
HTBT-CSV
