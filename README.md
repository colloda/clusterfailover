# clusterfailover

NOMES SERVIDORES:  
HOST1_CLT2  
HOST2_CLT2

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
