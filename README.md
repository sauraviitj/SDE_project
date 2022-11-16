Dynaspark
A research project called dynaSpark (Extended Spark) was initiated at Politecnico di Milano in 2016. It attempts to increase features for managing Spark applications' quality of service (QoS).

Users of dynaSpark can limit the amount of time Spark applications run by defining a deadline. Dynamically allocating resources (cores) will be done by dynaSpark to achieve the desired duration.


Executors are containerized using docker containers and assigned to a single stage in dynaSpark, which is built on a revolutionary container- and stage-based design. Additionally, dynaSpark employs distributed control theoretical planners for fine-grained CPU time allocation to each executor and a central heuristic to determine local deadlines for each stage.

DynaSpark was able to meet deadlines with an error rate of less than 1% during the experiments.


Apache Spark
A quick and versatile cluster computing technology for big data is called Spark. In addition to an engine that is efficient and enables general processing graphs for data analysis, it offers high-level APIs in Scala, Java, Python, and R. Additionally, a wide range of advanced tools are supported, such as Spark Streaming for stream processing, MLlib for machine learning, GraphX
Online Documentation
https://spark.apache.org/research.html
Building Spark
build/mvn -DskipTests clean package
Interactive Scala Shells
Starting Scala shell
./bin/spark-shell
Interactive Python Shell
Typical Programs
Additionally, the examples directory in Spark contains a number of sample programmes. Use the command./bin/run-example class> [params] to execute one of them. For instance:

./bin/run-example The Pi example will be run on-site via SparkPi.

When executing examples, you can set the MASTER environment variable to send those examples to a cluster. This can be a mesos:/ or spark:/ URL, with "yarn" for YARN, "local" for a single thread, or "local[N]" for N threads. If the class is located in the examples package, you may also use an abbreviated class name. For illustration
MASTER=spark://host:7077 ./bin/run-example SparkPi
If no parameters are provided, many of the example programmes print usage help.

Conducting tests
Spark must first be built before testing. Tests can be run using: once Spark has been built.

./dev/run-tests
Please refer to the instructions on how to run a module's tests or specific tests.
