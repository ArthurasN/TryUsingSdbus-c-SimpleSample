# TryUsingSdbus-cpp-SimpleSample
Its a test repository to try using sdbus-c++ library. 

Typical default D-Bus configuration does not allow to register services except explicitly allowed. You need to allow root to register your service. Create /etc/dbus-1/system.d/org.sdbuscpp.concatenator.conf

<!DOCTYPE busconfig PUBLIC
 "-//freedesktop//DTD D-BUS Bus Configuration 1.0//EN"
 "http://www.freedesktop.org/standards/dbus/1.0/busconfig.dtd">
<busconfig>
  <policy user="root">
    <allow own="org.sdbuscpp.concatenator"/>
    <allow send_destination="org.sdbuscpp.concatenator"
           send_interface="org.sdbuscpp.Concatenator"/>
  </policy>
</busconfig>
