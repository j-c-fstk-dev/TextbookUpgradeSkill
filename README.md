# TextbookUpgradeSkill

Uma skill modular para transformar materiais de ensino existentes em apostilas, atividades e roteiros de videoaula. Use uma etapa isolada ou combine as etapas para preparar um curso.

## Como usar

Abra [as instruções da skill](skills/textbook-upgrade/SKILL.md) com seu assistente de IA e forneça o material em um espaço de trabalho privado. Os arquivos deste repositório descrevem o método. Guarde originais, gravações, exemplos de clientes e resultados de projetos no espaço de cada autor.

Exemplos de pedido:

- “Faça apenas o diagnóstico destas páginas. Indique onde falta uma explicação que o professor costuma dar ao vivo.”
- “Reorganize este capítulo para iniciantes. Preserve os exemplos do instrutor e entregue uma atividade com resposta comentada.”
- “Use a ficha de aula aprovada para montar um roteiro de gravação. Temos uma câmera de celular e as duas fotos anexas.”

Comece por uma aula que o professor conhece bem. Compare o original e a versão revisada, se houver roteiro, leia-o em voz alta e registre as correções antes de ampliar para o curso inteiro.

## Começar com um único pedido

Anexe seu material em um espaço privado da IA e disponibilize a pasta completa da skill para que ela possa consultar os guias. Se o assistente aceitar apenas texto, cole as instruções e os guias relevantes na conversa.

> Melhore esta apostila para a minha turma. Examine os anexos, pergunte o que falta sobre o público, a marca e meu jeito de ensinar, e me ajude a escolher o layout. Prepare uma prova da apostila no formato combinado para eu avaliar. No final, reúna as decisões que ainda dependem de mim.

Se preferir delegar as escolhas visuais, diga “escolha a direção mais adequada”. Se quiser decidir, peça duas opções aplicadas ao mesmo trecho. A capacidade de gerar e conferir PDF ou arquivo editável depende da IA utilizada.

## Instalar no Codex CLI (Linux ou macOS)

Em uma nova instalação, execute no terminal. A pasta de instalação deve estar livre. O vínculo aponta para a skill do checkout, por isso mantenha a pasta do repositório.

```sh
git clone https://github.com/j-c-fstk-dev/TextbookUpgradeSkill.git "$HOME/TextbookUpgradeSkill" &&
mkdir -p "$HOME/.agents/skills" &&
test ! -e "$HOME/.agents/skills/textbook-upgrade" &&
ln -s "$HOME/TextbookUpgradeSkill/skills/textbook-upgrade" "$HOME/.agents/skills/textbook-upgrade"
```

Para atualizar e consultar a versão instalada:

```sh
git -C "$HOME/TextbookUpgradeSkill" pull --ff-only
cat "$HOME/.agents/skills/textbook-upgrade/VERSION"
```

Abra uma sessão do Codex na pasta privada do projeto. Exemplos para copiar:

- Iniciar: “Use $textbook-upgrade. Melhore esta apostila para minha turma.”
- Só apostila: “Prepare uma prova em PDF para iniciantes que leem no celular. Entregue prévias a 390 px.”
- Só vídeo: “Transforme este capítulo em um roteiro para gravar com uma câmera de celular.”
- Revisar: “Amplie as legendas da página 4. Exporte outra versão e preserve a prova anterior.”
- Aprovar: “Aprovo a diagramação. Aplique ao restante e mantenha as dúvidas técnicas na nota ao professor.”

## Usar no Codex sem acesso à internet

Baixe a [cópia completa em ZIP](https://github.com/j-c-fstk-dev/TextbookUpgradeSkill/archive/refs/heads/main.zip) em um navegador com acesso ao GitHub. Extraia a pasta `skills/textbook-upgrade` com todo o conteúdo e coloque-a como `textbook-upgrade/` na pasta privada da apostila que o Codex consegue ler.

> Leia textbook-upgrade/SKILL.md e as referências locais indicadas. Examine a apostila desta pasta e conduza a entrevista inicial. Quero melhorar a diagramação preservando o conteúdo.

Para PDFs escaneados, a skill orienta a testar a leitura e o reconhecimento de texto em páginas representativas antes de solicitar material adicional.

## Licença

Este projeto é distribuído sob a [GNU Affero General Public License, versão 3.0](LICENSE) (`AGPL-3.0-only`).
