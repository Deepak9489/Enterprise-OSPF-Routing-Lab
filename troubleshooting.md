# OSPF Troubleshooting

## R2-R3 Adjacency Incident

### Symptoms
Interfaces were up/up but R2-R3 ping failed and OSPF did not reach FULL.

### Checks
```cisco
show ip interface brief
ping 10.0.23.2
show ip ospf neighbor
show ip ospf interface brief
show ip route
```

### Root Cause
The R2-R3 physical connection was faulty/incorrect in the Packet Tracer lab.

### Corrective Action
The cable was replaced.

### Result
```text
R3-DC#ping 10.0.23.1
!!!!!
Success rate is 100 percent (5/5)
```

OSPF then reached FULL adjacency.

### Lesson
Troubleshoot in order:
Layer 1 -> Layer 2 -> Layer 3 -> Routing Protocol -> End-to-End.
