# wifi
$ git wifi configration
$ git Building configuration...
Current configuration : 723 bytes
!
version 12.4
no service pad
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption
!
hostname Router
!
boot-start-marker
boot-end-marker
!
logging message-counter syslog
!
no aaa new-model
!
no ipv6 cef
ip source-route
ip cef
!
!
!
!
multilink bundle-name authenticated
!
!
archive
log config
hidekeys
!
!
!
!
!
interface GigabitEthernet0/0
no ip address
shutdown
duplex auto
speed auto
!
interface GigabitEthernet0/1
no ip address
shutdown
duplex auto
speed auto
!
interface GigabitEthernet0/2
no ip address
shutdown
duplex auto
speed auto
!
ip forward-protocol nd
!
no ip http server
!
!
!
!
!
control-plane
!
!
line con 0
line aux 0
line vty 0 3
login
!
exception data-corruption buffer truncate
scheduler allocate 20000 1000
end
