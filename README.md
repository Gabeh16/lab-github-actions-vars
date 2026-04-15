Desafio GitHub Actions - Variáveis

Respostas

1. Por que a Secret aparece como `***` e a variável aparece normal?

Porque o GitHub protege automaticamente os secrets por segurança, mascarando seu valor nos logs. Já as variables não são sensíveis, então aparecem normalmente.

---

2. O Job deploy_app consegue ler a variável BUILD_VERSION do build_app? Por quê?

Não. Porque cada job roda em um ambiente separado (runner diferente), então as variáveis não são compartilhadas automaticamente entre jobs.
