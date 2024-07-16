# Perguntas e Respostas sobre Java e Microsserviços

## Fundamentos de Java

1. **O que é o Java Virtual Machine (JVM) e como ela funciona?**
   - A JVM é uma máquina virtual que executa bytecodes Java. Ela converte bytecodes em instruções de máquina específicas do sistema operacional e do hardware em que está sendo executada.

2. **Explique a diferença entre JDK, JRE e JVM.**
   - JDK (Java Development Kit) é um conjunto de ferramentas de desenvolvimento para criar aplicativos Java, incluindo JRE e ferramentas de desenvolvimento como compiladores e depuradores.
   - JRE (Java Runtime Environment) é um conjunto de ferramentas necessárias para executar aplicativos Java, incluindo a JVM, bibliotecas de classes e outros componentes.
   - JVM (Java Virtual Machine) é a parte do JRE que executa os bytecodes Java.

3. **O que são Generics em Java e por que eles são usados?**
   - Generics permitem que classes, interfaces e métodos operem em tipos específicos definidos pelo usuário, proporcionando maior segurança de tipos e eliminando a necessidade de casts explícitos.

4. **Qual a diferença entre Interface e Classe Abstrata em Java?**
   - Uma interface define um contrato que as classes implementadoras devem seguir, sem fornecer implementação de métodos. Uma classe abstrata pode fornecer tanto métodos abstratos quanto métodos com implementação.

5. **O que é Polimorfismo e como ele é implementado em Java?**
   - Polimorfismo é a capacidade de um objeto assumir muitas formas. Em Java, é implementado principalmente através de herança (classes) e interfaces, permitindo que uma referência de tipo superclasse seja usada para referenciar um objeto de subclasse.

6. **Explique o conceito de Imutabilidade em Java.**
   - Imutabilidade significa que, uma vez que um objeto é criado, seu estado não pode ser alterado. Classes como `String` e `Integer` são imutáveis em Java.

7. **O que é uma Collection em Java e quais são os principais tipos?**
   - Collections são estruturas de dados que armazenam grupos de objetos. Os principais tipos incluem `List`, `Set` e `Map`.

8. **Qual a diferença entre HashMap e TreeMap?**
   - `HashMap` é implementado usando uma tabela hash e não garante a ordem das chaves. `TreeMap` é implementado usando uma árvore binária de busca e mantém as chaves ordenadas.

9. **O que é o Garbage Collection em Java e como ele funciona?**
   - Garbage Collection é o processo automático de gerenciamento de memória que remove objetos não mais referenciados para liberar espaço na memória heap.

10. **Explique a diferença entre exceções verificadas e não verificadas.**
    - Exceções verificadas (checked) são aquelas que devem ser declaradas em um bloco `try-catch` ou lançadas na assinatura do método (`IOException`, por exemplo). Exceções não verificadas (unchecked) são aquelas que não precisam ser declaradas ou capturadas (`RuntimeException`, por exemplo).

## Programação Concorrente

11. **O que são Threads em Java?**
    - Threads são unidades de execução dentro de um processo. Em Java, elas são representadas pela classe `Thread` e pela interface `Runnable`.

12. **Explique a diferença entre o método `synchronized` e a classe `ReentrantLock`.**
    - O método `synchronized` é um mecanismo de sincronização simples que bloqueia um objeto ou método. `ReentrantLock` é uma classe mais flexível que oferece bloqueios explícitos com opções adicionais como bloqueios justos e não justos.

13. **O que é o Executor Framework em Java?**
    - O Executor Framework é uma API que simplifica a execução de tarefas assíncronas e fornece um mecanismo para gerenciamento de threads em pools.

14. **Como você evitaria condições de corrida em um programa Java?**
    - Usando mecanismos de sincronização como blocos `synchronized`, `ReentrantLock`, `Atomic` classes e garantindo que as operações críticas sejam realizadas de maneira atômica.

15. **O que é o Fork/Join Framework em Java?**
    - É um framework para dividir tarefas grandes em subtarefas menores que podem ser executadas em paralelo, utilizando um pool de threads.

## Microsserviços

16. **O que são microsserviços e como eles se diferenciam da arquitetura monolítica?**
    - Microsserviços são uma arquitetura de software onde aplicações são compostas por serviços pequenos, independentes e implantáveis separadamente. Diferente da arquitetura monolítica, onde toda a aplicação é construída como um único bloco.

17. **Quais são as vantagens e desvantagens dos microsserviços?**
    - Vantagens: Escalabilidade, desenvolvimento e implantação independentes, facilidade de manutenção. Desvantagens: Complexidade de gerenciamento, desafios de comunicação entre serviços, problemas de consistência de dados.

18. **Explique o conceito de API Gateway em uma arquitetura de microsserviços.**
    - API Gateway é um ponto de entrada único para todas as requisições de cliente, que roteia essas requisições para os microsserviços apropriados e pode fornecer funcionalidades como autenticação, logging e balanceamento de carga.

19. **Como você lidaria com a comunicação entre microsserviços?**
    - Usando protocolos de comunicação síncrona (HTTP/REST, gRPC) ou assíncrona (mensageria com RabbitMQ, Kafka).

20. **O que é Service Discovery e por que ele é importante em microsserviços?**
    - Service Discovery é o processo pelo qual serviços encontram outros serviços na rede. É importante para a escalabilidade e flexibilidade, permitindo que serviços se registrem e descubram dinamicamente.

21. **O que é o padrão Circuit Breaker e como ele é implementado?**
    - Circuit Breaker é um padrão de design usado para detectar falhas e encapsular a lógica de recuperação, permitindo que a aplicação continue a funcionar corretamente. Pode ser implementado usando bibliotecas como Hystrix ou Resilience4j.

22. **Como você monitoraria e faria o logging de microsserviços?**
    - Usando ferramentas de monitoramento (Prometheus, Grafana), logging centralizado (ELK stack) e tracing distribuído (Jaeger, Zipkin).

23. **Explique o conceito de "eventual consistency" em microsserviços.**
    - Eventual consistency é um modelo de consistência onde o sistema garante que, eventualmente, todos os nós terão uma visão consistente dos dados, mesmo que não imediatamente após uma operação.

24. **O que são Sagas e como elas são usadas para gerenciar transações em microsserviços?**
    - Sagas são um padrão para gerenciar transações distribuídas em microsserviços, onde cada serviço realiza uma transação local e publica um evento ou executa uma ação compensatória em caso de falha.

25. **Como você implementaria segurança em uma arquitetura de microsserviços?**
    - Usando autenticação e autorização (OAuth2, JWT), encriptação de dados em trânsito e em repouso, e práticas de segurança como controle de acesso e auditoria.

## Ferramentas e Tecnologias

26. **O que é Spring Boot e como ele facilita o desenvolvimento de microsserviços?**
    - Spring Boot é um framework que simplifica a configuração e o desenvolvimento de aplicativos Java, oferecendo uma série de convenções e bibliotecas prontas para uso, tornando mais fácil criar microsserviços.

27. **Explique o que são Spring Cloud e seus componentes principais.**
    - Spring Cloud é um conjunto de ferramentas para construir aplicações distribuídas. Componentes principais incluem Spring Cloud Config (configuração centralizada), Eureka (Service Discovery), Ribbon (load balancing), e Hystrix (Circuit Breaker).

28. **O que é Docker e como ele é usado em microsserviços?**
    - Docker é uma plataforma de containers que permite empacotar, distribuir e executar aplicativos de forma isolada. Em microsserviços, Docker facilita a criação de ambientes consistentes e portáteis.

29. **O que é Kubernetes e como ele auxilia na orquestração de microsserviços?**
    - Kubernetes é um sistema de orquestração de containers que automatiza a implantação, o dimensionamento e a operação de aplicativos em containers, facilitando a gestão de microsserviços.

30. **Como você versionaria e faria deploy de microsserviços?**
    - Usando sistemas de controle de versão (Git), e pipelines de CI/CD (Jenkins, GitLab CI) para automatizar o build, teste e deploy. Versionamento semântico e práticas de deployment como Blue-Green e Canary deployments são comumente usadas.

## Testes e Qualidade

31. **Como você testaria microsserviços?**
    - Usando testes unitários, testes de integração, testes de contrato, e testes end-to-end. Ferramentas como JUnit, Mockito, WireMock, e Postman podem ser usadas.

32. **O que são testes de contrato em microsserviços?**
    - Testes de contrato verificam que a comunicação entre serviços cumpre os contratos estabelecidos, garantindo que alterações em um serviço não quebrem outros serviços dependentes.

33. **Como você garantiria a resiliência e a tolerância a falhas dos microsserviços?**
    - Implementando padrões como Circuit Breaker, Bulkhead, e Retry. Usando ferramentas de monitoramento e práticas de Chaos Engineering para testar a resiliência.

34. **O que é o Chaos Engineering e como ele se aplica a microsserviços?**
    - Chaos Engineering é a prática de introduzir falhas controladas no sistema para identificar e mitigar problemas antes que ocorram em produção. Em microsserviços, ajuda a validar a resiliência e a tolerância a falhas.

## Práticas e Padrões

35. **O que é o padrão API First?**
    - API First é uma abordagem onde a definição da API é a primeira etapa do desenvolvimento, garantindo que a API seja bem projetada e servindo como contrato para a implementação.

36. **Como você gerenciaria configurações em uma arquitetura de microsserviços?**
    - Usando um serviço de configuração centralizado, como Spring Cloud Config ou Consul, permitindo a gestão de configurações de forma dinâmica e centralizada.

37. **O que são Sidecars e como eles são usados em microsserviços?**
    - Sidecars são contêineres auxiliares que acompanham o serviço principal e fornecem funcionalidades adicionais, como logging, proxy, e monitoramento, sem alterar o código do serviço principal.

38. **Explique a importância da automação na CI/CD para microsserviços.**
    - A automação na CI/CD permite integração, teste e implantação contínuos, garantindo que mudanças no código sejam entregues de maneira rápida e confiável, essencial para a agilidade e a consistência em arquiteturas de microsserviços.

39. **Como você gerenciaria a escalabilidade dos microsserviços?**
    - Usando escalonamento automático (auto-scaling) com ferramentas como Kubernetes, balanceamento de carga, e práticas de design como desacoplamento de serviços e particionamento de dados.

40. **O que é o padrão Strangler Fig e como ele é aplicado na migração para microsserviços?**
    - Strangler Fig é um padrão de migração onde novas funcionalidades são desenvolvidas como microsserviços que gradualmente substituem partes do sistema monolítico, até que o monólito seja totalmente substituído.

## Banco de Dados

41. **Como você lidaria com a persistência de dados em microsserviços?**
    - Usando bancos de dados independentes para cada serviço (Database per Service) para evitar o acoplamento, e utilizando eventos para sincronização de dados quando necessário.

42. **O que é o padrão Database per Service?**
    - Cada serviço possui seu próprio banco de dados privado, evitando dependências diretas entre serviços e permitindo que cada serviço escolha a tecnologia de banco de dados que melhor se adequa às suas necessidades.

43. **Explique a diferença entre uma transação distribuída e uma transação local.**
    - Uma transação local é gerida por um único banco de dados. Uma transação distribuída envolve múltiplos recursos ou serviços, exigindo coordenação para garantir a consistência entre todos os participantes.

44. **Como você lidaria com migrações de banco de dados em uma arquitetura de microsserviços?**
    - Usando ferramentas de migração de banco de dados (Flyway, Liquibase) e práticas de migração como migrações blue-green, evitando downtime e garantindo que a aplicação continue a funcionar durante a migração.

## Diversos

45. **O que são contratos de API e como você garantiria a compatibilidade entre versões?**
    - Contratos de API definem as expectativas de comunicação entre serviços. A compatibilidade entre versões pode ser garantida usando versionamento de API, testes de contrato, e práticas de compatibilidade retroativa.

46. **Como você gerenciaria a configuração centralizada em microsserviços?**
    - Usando serviços como Spring Cloud Config, Consul, ou etcd, que permitem armazenar e gerenciar configurações centralizadas e distribuí-las dinamicamente para os microsserviços.

47. **Explique o conceito de backpressure e como ele pode ser gerenciado.**
    - Backpressure é a capacidade de um sistema de controlar a taxa de entrada de requisições para evitar sobrecarga. Pode ser gerenciado usando filas, buffers, e padrões de controle de fluxo.

48. **O que é o padrão Bulkhead e como ele ajuda na resiliência de microsserviços?**
    - Bulkhead é um padrão que isola partes de um sistema para evitar que uma falha em uma parte se propague para outras. Em microsserviços, pode ser implementado separando recursos (threads, pools de conexão) por serviço.

49. **Como você integraria serviços legados em uma arquitetura de microsserviços?**
    - Usando adaptadores ou "anti-corruption layers" que encapsulam a lógica do sistema legado e expõem interfaces compatíveis com os microsserviços.

50. **Explique o conceito de observabilidade e como ele se aplica a microsserviços.**
    - Observabilidade é a capacidade de medir o estado interno de um sistema com base na sua saída externa. Em microsserviços, envolve o uso de logging, métricas, e tracing distribuído para monitorar e entender o comportamento do sistema.
