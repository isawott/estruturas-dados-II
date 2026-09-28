# Revisão de Estrutura de Árvores

**Nome:** Giovanna Nascimento Lima
**Disciplina:** Estrutura de Dados II
**Professora:** Profa. Kadidja Valéria
**Turma:** D1

---

# Etapa 1 — Revisão bibliográfica

## Conceitos básicos de árvores

Uma árvore é uma estrutura de dados utilizada para representar informações de maneira **hierárquica**. Ela é formada por nós, sendo que existe um nó principal chamado **raiz**. Os nós ligados diretamente a outro nó são seus filhos, enquanto o nó acima é chamado de pai. Os nós que não possuem filhos são chamados de folhas.

Uma árvore possui um único caminho entre a raiz e qualquer outro nó. A **altura** corresponde ao comprimento do caminho mais longo da raiz até uma folha.

## Árvore geral

Uma árvore geral, também chamada de árvore genérica, permite que cada nó tenha um número **arbitrário de filhos**. Portanto, não existe a limitação de dois filhos existente nas árvores binárias.

Esse tipo de estrutura pode ser utilizado para representar uma hierarquia de diretórios, por exemplo, em que um diretório pode possuir vários subdiretórios.

## Árvore binária

Na árvore binária, cada nó pode possuir **zero, um ou dois filhos**. Os filhos são identificados como filho esquerdo e filho direito.

Uma árvore binária comum não precisa possuir uma ordenação específica dos valores.

## Árvore Binária de Busca (ABB)

A Árvore Binária de Busca, ou ABB, é uma árvore binária que utiliza a posição dos valores para facilitar a busca.

Na organização apresentada em aula, valores **menores que o nó atual ficam à esquerda**, enquanto valores **maiores ficam à direita**. Durante uma busca, cada comparação determina qual subárvore deve ser seguida.
Na inserção, as comparações são repetidas até que seja encontrada uma posição vazia para o novo nó.

## Árvore AVL

A AVL é uma árvore binária de busca balanceada. Seu objetivo é manter a altura da árvore controlada para evitar que ela fique muito desequilibrada.

Quando uma alteração provoca desequilíbrio, são utilizadas **rotações** para reorganizar a árvore.

**Observação:** o material de Celes e Rangel e os slides da aula enviados não apresentam a árvore AVL em detalhes. A descrição acima corresponde ao conceito geral da estrutura.

## Árvore Rubro-Negra

A árvore rubro-negra é uma árvore de busca que utiliza **cores associadas aos nós**, normalmente vermelho e preto, para controlar o balanceamento da árvore.

Após determinadas alterações, podem ser realizadas recolorações e rotações para preservar as propriedades da estrutura.

**Observação:** os dois materiais enviados não apresentam o funcionamento detalhado da árvore rubro-negra.

## Árvore B

A árvore B é uma estrutura de busca na qual um mesmo nó pode armazenar **várias chaves**. Quando um nó fica cheio, pode ocorrer uma divisão para manter a organização da árvore.

É utilizada principalmente para trabalhar com grandes quantidades de dados e estruturas de armazenamento.

**Observação:** os dois materiais enviados não apresentam a árvore B em detalhes.

## Árvore B+

A árvore B+ é uma estrutura semelhante à árvore B, porém os registros ficam concentrados nas **folhas**. As folhas podem ser ligadas entre si, facilitando consultas sequenciais e consultas por intervalo.

**Observação:** os dois materiais enviados não apresentam a árvore B+ em detalhes.

## Heap

O heap é uma estrutura organizada de acordo com uma propriedade de prioridade. No **max-heap**, o maior elemento fica na raiz; no **min-heap**, o menor elemento fica na raiz.

Pode ser utilizado em filas de prioridade e em algoritmos de ordenação.

**Observação:** os dois materiais enviados não apresentam o heap em detalhes.

## Trie

A trie é uma árvore utilizada para armazenar e pesquisar palavras ou sequências de caracteres. Os caracteres são organizados em níveis e palavras que possuem o mesmo prefixo podem compartilhar parte do caminho.

Pode ser utilizada em buscas de palavras e sistemas de sugestões.

**Observação:** os dois materiais enviados não apresentam a trie em detalhes.

---

# Etapa 2 — Quadro comparativo

| Estrutura          | Organização dos dados                                       | Regra ou propriedade principal                                 | Operação ou ajuste importante             | Exemplo de aplicação                                   | Referência consultada                                             |
| ------------------ | ----------------------------------------------------------- | -------------------------------------------------------------- | ----------------------------------------- | ------------------------------------------------------ | ----------------------------------------------------------------- |
| **Árvore geral**   | Um nó pode possuir vários filhos.                           | Não existe limite fixo de filhos por nó.                       | Inserção, busca e remoção de subárvores.  | Estrutura de diretórios.                               | Celes e Rangel, *Estruturas de Dados — Árvores*, cap. 13          |
| **Árvore binária** | Cada nó possui no máximo dois filhos.                       | Os filhos são organizados como subárvore esquerda e direita.   | Inserção, busca, remoção e percursos.     | Representação de expressões e estruturas hierárquicas. | Celes e Rangel, *Estruturas de Dados — Árvores*, cap. 13          |
| **ABB**            | Valores menores ficam à esquerda e maiores à direita.       | A ordenação orienta o caminho da busca.                        | Inserção e busca por comparações.         | Busca eficiente de valores.                            | Aula “Árvores simples e busca básica”, UDF, 14/09                 |
| **AVL**            | Árvore binária de busca balanceada.                         | A altura deve permanecer controlada.                           | Rotações para corrigir desequilíbrios.    | Estruturas que precisam de busca eficiente.            | Conteúdo geral da estrutura; não detalhado nos materiais enviados |
| **Rubro-negra**    | Árvore de busca com nós associados a cores.                 | As propriedades das cores ajudam a controlar a altura.         | Recolorações e rotações.                  | Estruturas de busca balanceadas.                       | Conteúdo geral da estrutura; não detalhado nos materiais enviados |
| **B**              | Um nó pode armazenar várias chaves.                         | A árvore mantém os nós organizados e balanceados.              | Divisão de nós quando necessário.         | Índices e armazenamento de grandes volumes de dados.   | Conteúdo geral da estrutura; não detalhado nos materiais enviados |
| **B+**             | Chaves em nós internos e registros concentrados nas folhas. | As folhas podem ser ligadas para facilitar consultas.          | Divisão de nós e manutenção das folhas.   | Índices e consultas por intervalo.                     | Conteúdo geral da estrutura; não detalhado nos materiais enviados |
| **Heap**           | Elementos são organizados por prioridade.                   | A raiz possui a maior ou menor prioridade, dependendo do tipo. | Reorganização após inserção ou remoção.   | Fila de prioridade.                                    | Conteúdo geral da estrutura; não detalhado nos materiais enviados |
| **Trie**           | Caracteres são organizados em níveis.                       | Palavras com prefixos iguais compartilham caminhos.            | Inserção e busca caractere por caractere. | Busca e sugestões de palavras.                         | Conteúdo geral da estrutura; não detalhado nos materiais enviados |

---

# Etapa 3 — Identificação por analogias

## 1. Uma estante de números é reorganizada por rotações quando um lado fica alto demais em relação ao outro.

**Estrutura: Árvore AVL**

A situação representa uma árvore AVL porque essa estrutura utiliza o balanceamento para evitar que um lado da árvore fique muito mais alto que o outro. Quando ocorre um desequilíbrio, podem ser utilizadas rotações para reorganizar a estrutura.

**Limite da analogia:** uma estante física não possui uma regra matemática de balanceamento. A comparação representa somente a ideia de reorganização para manter os lados equilibrados.

---

## 2. Um catálogo guarda várias chaves por página; quando uma página fica cheia, ela é dividida.

**Estrutura: Árvore B**

A situação representa uma árvore B porque essa estrutura permite armazenar várias chaves em um mesmo nó. Quando um nó fica cheio, ele pode ser dividido para manter a organização da árvore.

**Limite da analogia:** uma página de um catálogo físico não realiza automaticamente as operações de divisão e reorganização que acontecem em uma estrutura de dados.

---

## 3. Uma fila mantém a tarefa de maior prioridade no topo para retirá-la primeiro.

**Estrutura: Heap**

A situação representa um heap, principalmente um **max-heap**, porque o elemento de maior prioridade permanece na raiz e pode ser retirado primeiro.

**Limite da analogia:** uma fila física representa a ideia de prioridade, mas não necessariamente possui a estrutura hierárquica de um heap.

---

## 4. Um índice percorre letras sucessivas e compartilha o início das palavras de mesmo prefixo.

**Estrutura: Trie**

A situação representa uma trie porque os caracteres são organizados em diferentes níveis e palavras que possuem o mesmo prefixo podem compartilhar os mesmos caminhos iniciais.

**Limite da analogia:** um índice comum não necessariamente possui a organização em nós e caracteres de uma trie.

---

## 5. Uma estrutura usa cores, recolorações e rotações para manter controlada a altura dos caminhos de busca.

**Estrutura: Árvore Rubro-Negra**

A situação representa uma árvore rubro-negra porque essa estrutura utiliza cores, recolorações e rotações para preservar suas propriedades e controlar a altura dos caminhos de busca.

**Limite da analogia:** as cores representam propriedades lógicas dos nós e não cores físicas utilizadas para organizar objetos.

---

## 6. Um índice conduz às folhas que contêm os registros, ligadas entre si para facilitar consultas por intervalo.

**Estrutura: Árvore B+**

A situação representa uma árvore B+ porque os registros ficam nas folhas e essas folhas podem ser ligadas entre si. Essa organização facilita consultas sequenciais e consultas por intervalo.

**Limite da analogia:** um índice real pode possuir outros mecanismos de armazenamento que não aparecem na representação simplificada da árvore B+.

---

## 7. Numa coleção de números, cada nó direciona valores menores para a esquerda e maiores para a direita.

**Estrutura: Árvore Binária de Busca (ABB)**

A situação representa uma ABB porque sua regra de organização coloca os valores **menores à esquerda** e os valores **maiores à direita** do nó atual. Essa organização permite que a comparação determine qual caminho deve ser seguido durante a busca.

**Limite da analogia:** a regra de menores à esquerda e maiores à direita não garante que a árvore esteja equilibrada. A forma da árvore depende da ordem de inserção e pode influenciar o custo da busca.

---

# Referências consultadas

1. **CELES, Waldemar; RANGEL, José L.** *Estruturas de Dados — 13. Árvores*. PUC-Rio. Material de apoio disponibilizado para a disciplina. O material aborda árvores, árvores binárias, árvores genéricas, altura, busca e percursos.

2. **VALÉRIA, Kadidja.** *Árvores simples e busca básica*. Estrutura de Dados II — Ciência da Computação, UDF, 14 de setembro. Material de aula. O material aborda conceitos de árvores, árvore binária, ABB, inserção e busca.

3. **VALÉRIA, Kadidja.** *Revisão de estrutura de árvores*. Atividade individual remota de Estrutura de Dados II, 28/09. Material fornecido pela disciplina.
