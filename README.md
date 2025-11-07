# AulaGit
1. O que é CI/CD e por que é importante?

💡 Resposta:
CI/CD é um conjunto de práticas que automatiza a integração e entrega de software.

CI (Continuous Integration) → integra o código continuamente e executa testes a cada alteração.

CD (Continuous Delivery/Deployment) → automatiza a entrega ou implantação do software.
É importante porque reduz erros, acelera o desenvolvimento, garante mais qualidade e detecta problemas cedo.



---

2. Em qual pasta os workflows do GitHub ficam armazenados?

💡 Resposta:
Na pasta:

.github/workflows/


---

✅ Perguntas da etapa de execução do pipeline

1. O que aparece no log do GitHub Actions após a execução?

💡 Resposta:
O log mostra cada etapa do workflow sendo executada, incluindo:

Checkout do código

Configuração do Python

Execução do script main.py
E o output final exibirá:


Hello CI/CD!


---

2. O que acontece se alterar o código e fizer novo push?

💡 Resposta:
O GitHub Actions dispara novamente o workflow automaticamente e executa todo o pipeline com a nova versão do código.


---

✅ Pergunta extra — testes

O que acontece se um teste falhar?

💡 Resposta:
O workflow é marcado como FAILED, o job para na etapa do teste e o log mostra qual teste falhou.
Isso impede que o código avance para etapas posteriores (como deploy).


---

✅ 4. Para finalizar

Como o GitHub Actions ajuda a detectar erros cedo?

💡 Resposta:
Porque ele roda automaticamente testes, validações e builds a cada push. Assim, erros são identificados no momento em que o código é enviado, evitando que cheguem à produção.


---

Quais seriam exemplos reais de CI/CD em projetos web ou mobile?

💡 Resposta:

Publicar automaticamente um site React no Vercel ou Netlify.

Rodar testes e gerar APK/IPA de apps no Flutter a cada push.

Deploy automático de APIs para Render, Heroku, Railway ou AWS.

Build automatizado de containers Docker e envio para o Docker Hub.



---

Como o deploy automático poderia ser feito a partir deste pipeline?

💡 Resposta:
Adicionando um novo job no workflow, por exemplo:

Fazer deploy para um serviço (Render, Vercel, Firebase, AWS, etc).

Usar secrets do GitHub (API_KEY, TOKEN, etc).

Executar scripts como:


npm run build
vercel --prod

ou

docker build ...
docker push ...

Dependendo da plataforma.
