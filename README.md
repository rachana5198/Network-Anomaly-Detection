# Network Anomaly Detection
In this repo, anomalies in computer network are detected based on the patterns in the data using K-Nearest Neighbours algorithm and data are clustered into similar attack type using k-means algorithm.
## Understanding the dataset

### Feature Name(Type) - Description

#### Features of individual TCP connections
1. Duration(continuous) - length (number of seconds) of the connection
2. protocol_type(discrete) - type of the protocol, e.g. tcp, udp, etc.
3. service(discrete) - network service on the destination, e.g., http, telnet, etc.
4. src_bytes(continuous) - number of data bytes from source to destination
5. dst_bytes(continuous) - number of data bytes from destination to source
6. flag(discrete) - normal or error status of the connection
7. land(discrete) - 1 if connection is from/to the same host/port; 0 otherwise
8. wrong_fragment(continuous) - number of wrong fragments
9. urgent(continuous) - number of urgent packets

#### Features within a connection suggested by domain knowledge

1. hot(continuous) - number of hot indicators
2. num_failed_logins(continuous) - number of failed login attempts
3. logged_in(discrete) - 1 if successfully logged in; 0 otherwise
4. num_compromised(continuous) - number of compromised conditions
5. root_shell(discrete) - 1 if root shell is obtained; 0 otherwise
6. su_attempted(discrete) - 1 if su root command attempted; 0 otherwise
7. num_root(continuous) - number of root accesses
8. num_file_creations(continuous) - number of file creation operations
9. num_shells(continuous) - number of shell prompts
10. num_access_files(continuous) - number of operations on access control files
11. num_outbound_cmds(continuous) - number of outbound commands in an ftp session
12. is_hot_login(discrete) - 1 if the login belongs to the "hot" list; 0 otherwise
13. is_guest_login(discrete) - 1 if the login is a "guest" login; 0 otherwise

#### Traffic features computed using a two-second time window

1. count(continuous) - number of connections to the same host as the current connection in the past two seconds
2. serror_rate(continuous) - % of connections that have "SYN" errors
3. rerror_rate(continuous) - % of connections that have "REJ" errors
4. same_srv_rate(continuous) - % of connections to the same service
5. diff_srv_rate(continuous) - % of connections to different services
6. srv_count(continuous) - number of connections to the same service as the current connection in the past two seconds
7. srv_serror_rate(continuous) - % of connections that have "SYN" errors
8. srv_rerror_rate(continuous) - % of connections that have "REJ" errors
9. srv_diff_host_rate(continuous) - % of connections to different hosts 
