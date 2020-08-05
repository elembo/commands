# Swiss Army of Commands

## Ingress PE

show pim vrf xxxx interface  
show pim vrf xxxx neighbors <<<<< Not all Profiles need to see PIM Neighbors  
show pim vrf xxxx topology A.B.C.D\
show pim vrf xxxx mdt cache X.Y.W.Z | in A.B.C.D <<<< X.Y.W.Z is Ingress PE and A.B.C.D the Mcast Group\
show mrib vrf xxxx route A.B.C.D detail\
show mpls mldp database p2mp root <<X.Y.W.Z>> opaquetype << mdt id >> detail <<<< X.Y.W.Z is Ingress PE and mdt id either mdt or global id\
6.6 xxxxx detail <<<< use local label from mdt data <<<<\
show mpls forwarding labels xxxxx detail\
show mpls forwarding labels xxxxx hardware ingress/egress detail location x/x/cpu0\
show controllers mgidprgm mgidindex yyyyy location x/x/cpu0 <<<<<<< where yyyyy is the mgid id from previous output.\

Egress PE

show igmp vrf xxxx group A.B.C.D\


show igmp vrf xxxx interface\
show pim vrf xxxx interface\
show pim vrf xxxx neighbors <<<<< Not all Profiles need to see PIM Neighbors\
show pim vrf xxxx topology A.B.C.D\
show pim vrf xxxx mdt cache X.Y.W.Z | in A.B.C.D <<<< X.Y.W.Z is Ingress PE and A.B.C.D the Mcast Group\
show mrib vrf xxxx route A.B.C.D detail\
show mpls mldp database p2mp root <<X.Y.W.Z>> opaquetype << mdt id >> detail <<<< X.Y.W.Z is Ingress PE and mdt id either mdt or global id\
show mrib mpls forwarding labels xxxxx detail <<<< use local label from mdt data <<<<\
show mpls forwarding labels xxxxx detail\
show mpls forwarding labels xxxxx hardware ingress/egress detail location x/x/cpu0\
show controllers mgidprgm mgidindex yyyyy location x/x/cpu0 <<<<<<< where yyyyy is the mgid id from previous output.\

 
CORE


show mpls mldp database p2mp root <<X.Y.W.Z>> opaquetype << mdt id >> detail <<<< X.Y.W.Z is Ingress PE and mdt id either mdt or global id\
show mrib mpls forwarding labels xxxxx detail <<<< use local label from mdt data <<<<\
show mpls forwarding labels xxxxx detail\
show mpls forwarding labels xxxxx hardware ingress/egress detail location x/x/cpu0\
show controllers mgidprgm mgidindex yyyyy location x/x/cpu0 <<<<<<< where yyyyy is the mgid id from previous output.\
 
BGP Signaling (Mcast vpn NLRI)


show bgp ipv4 mvpn vrf xxxxx route-type 1 --> each PE in the VRF will generate its own T-1\
show bgp ipv4 mvpn vrf xxxxx route-type 3 --> MDT Data, advertisment by Ingress PE, and *,* advertise by Egress PE\
show bgp ipv4 mvpn vrf xxxxx route-type 5 --> S,G Advertisment >>>> Ingress PE originates it.\
show bgp ipv4 mvpn vrf xxxxx route-type 6 --> *,G Join <<< Egress PE originates it\
show bgp ipv4 mvpn vrf xxxxx route-type 7 --> S,G Join <<< Egress PE originate it in SSM << PE connected to PIM-RP originates it in SM\

Generic


admin show diag chassis eeprom-info\
show igmp vrf xxxx ranges\

show pim vrf xxxx context private detail\
show pim vrf xxxx range-list\
show pim vrf xxxxx rp mapping\
show mgid client mapping name mribv4\
show mpls ldp capability\
show mpls ldp neighbors\
show mpls mldp status\
show mpls mldp root\
show mpls mldp database brief\
show mpls forwarding p2mp\
show mpls forwarding labels <LABEL> hardware ingress detail location <LCs>\
show mpls forwarding labels <LABEL> hardware egress detail location <LCs>\
show mpls forwarding labels <LABEL> detail debug\
show mpls forwarding labels <LABEL> detail debug location <LC>\

 
Show Techs


show tech multicast address-family ipv4/ipv6\
show tech multicast address-family ipv4/ipv6 vrf <>\
show tech multicast address-family ipv4/ipv6 hardware\
show tech mgid\
show tech pfi\
show tech bundle\
show tech np\
show tech-support mpls lsd\
show tech mpls ldp\
show tech cef\
show tech cef platform\
show log\
