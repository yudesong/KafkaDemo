#Kafka Java API案例
<h3>Producer</h3>
可选配置，如果不配置，则使用默认的partitioner根据key值value映射到指定的Parition  
props.put("partitioner.class", "kafka.demo.PartitionerDemo"); 
<h3>Consumer</h3>
String key=(String)obj;  
int offset = key.lastIndexOf('.');  
if(offset>0){  
partition = Integer.parseInt(key.substring(offset + 1)) % numPartitions；
}


