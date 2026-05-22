# Erros Identificados

Durante a análise do módulo de gerenciamento de alunos, identificamos um erro crítico de **execução (Runtime)** e **lógica** no método de busca por ID.

### Trecho do Código Problemático

```java
@RestController
@RequestMapping("/alunos")
public class AlunoController {

    @Autowired
    private AlunoRepository repository;

    @GetMapping("/{id}")
    public Aluno buscarPorId(@PathVariable Long id) {
        // Erro: Se o ID não existir, o findById().get() lança NoSuchElementException
        // Além disso, expõe a entidade diretamente sem um tratamento HTTP adequado
        return repository.findById(id).get();
    }
}