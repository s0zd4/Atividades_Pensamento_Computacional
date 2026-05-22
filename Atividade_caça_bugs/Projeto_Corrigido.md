# Projeto Corrigido

Para sanar o problema de busca e melhorar a API, implementamos uma exceção personalizada e um manipulador global de erros (`@ControllerAdvice`) no Spring Boot.

### Código Corrigido

#### 1. Criação da Exceção Personalizada
```java
public class ResourceNotFoundException extends RuntimeException {
    public ResourceNotFoundException(String mensagem) {
        super(mensagem);
    }
}