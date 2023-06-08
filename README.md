# demo-redis

Demo Spring Security (v2.7.11) project for testing Redis Insight v2.26, when Serialized Java objects stored in redis.
For simplicity, sample users are stored in-memory (see `/config/SecurityConfig.java`), and not in a persistent database.

## Requirements

- Java JDK 8 or higher
- Redis server v6.0 or higher
- Any web browser

## How to use

1. Edit file [application.yml](src/main/resources/application.yml), with your Redis credentials
2. Run project using either your Java IDE (any can work), or command-line (`./mvnw spring-boot:run`)
3. Open your browser to http://localhost:9000/login
4. Login with username `demo` and pass `p@ssword`. Session should be stored in redis now.
5. Check RedisInsight, refresh. Change format to JAVA serialized.
6. Done. Observe scrambled characters, especially for **SETS** and **HASH** .