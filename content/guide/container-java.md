# Container readiness for Java applications

Always specify an -Xmx since Java can't detect the containers memory size and will auto-set the maximum heap size based on the container hosts available memory. This could result in a massive overallocation of memory and unpredictable crashes.

Until this is [fixed|https://www.infoq.com/news/2017/02/java-memory-limit-container] in Java 9, remember to set the -Xmx for every Java application running in a container.