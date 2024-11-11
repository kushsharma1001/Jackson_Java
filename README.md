# Jackson_Java
Serialization/DeSerialization of object to Json in java using Jackson

https://www.novixys.com/blog/jackson-annotations-guide/

https://shekhargulati.com/2018/05/07/til-3-exclude-null-fields-in-spring-boot-rest-json-api-serializing-enum-value-with-jackson-and-change-remote-for-a-branch-in-git/

https://mkyong.com/java/jackson-how-to-ignore-null-fields/

https://www.baeldung.com/jackson-object-mapper-tutorial

1. @JsonIgnore at field level ignores that field and @JsonIgnoreProperties() lets us ignore multiple fields.
2. @JsonInclude(JsonInclude.Include.NON_NULL)
3. String to JSON Object:
   String json = "{\"name\": \"mkyong\", \"age\": 20}";
   Person obj = mapper.readValue(json, Person.class);
  
5. Object to String:
       Person person = new Person("mkyong", 42);
       ObjectMapper om = new ObjectMapper();

        try {

            // covert Java object to JSON strings
            String json = om.writeValueAsString(person);

            // output: {"name":"mkyong","age":42}
            System.out.println(json);

        } catch (JsonProcessingException e) {
            throw new RuntimeException(e);
        }
