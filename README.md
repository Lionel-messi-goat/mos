
DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
Traceback (most recent call last):
  File "/home/pi/pj/Project.py", line 19, in <module>
    client.connect(mqtt_broker_ip, 1883, 60)
  File "/home/pi/myenv/lib/python3.9/site-packages/paho/mqtt/client.py", line 1435, in connect
    return self.reconnect()
  File "/home/pi/myenv/lib/python3.9/site-packages/paho/mqtt/client.py", line 1598, in reconnect
    self._sock = self._create_socket()
  File "/home/pi/myenv/lib/python3.9/site-packages/paho/mqtt/client.py", line 4609, in _create_socket
    sock = self._create_socket_connection()
  File "/home/pi/myenv/lib/python3.9/site-packages/paho/mqtt/client.py", line 4640, in _create_socket_connection
    return socket.create_connection(addr, timeout=self._connect_timeout, source_address=source)
  File "/usr/lib/python3.9/socket.py", line 843, in create_connection
    raise err
  File "/usr/lib/python3.9/socket.py", line 831, in create_connection
    sock.connect(sa)
ConnectionRefusedError: [Errno 111] Connection refused
