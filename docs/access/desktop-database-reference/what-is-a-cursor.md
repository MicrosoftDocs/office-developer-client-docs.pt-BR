---
title: O que é um Cursor?  (Referência de banco de dados da área de trabalho do access)
TOCTitle: What is a Cursor?
ms:assetid: cc70d941-05e0-9b14-1c5d-6b1a5802f546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250013(v=office.15)
ms:contentKeyID: 48547738
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0bedbeb041d919cd417ade215ac71b9eabbc4de2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947592"
---
# <a name="what-is-a-cursor"></a>O que é um cursor?


**Aplica-se a**: Access 2013, o Office 2013

As operações em um banco de dados relacional agem em um conjunto completo de linhas. O conjunto de linha retornado por uma instrução SELECT é composto por todas as linhas que atendem às condições na cláusula WHERE da instrução. Esse conjunto completo de linhas retornado pela instrução é conhecido como o conjunto de resultados. Os aplicativos, especialmente aqueles que são interativos e estão online, nem sempre podem trabalhar de forma eficiente com um conjunto inteiro de resultados como uma unidade. Esses aplicativos precisam de um mecanismo para trabalharem com uma linha ou um pequeno bloco de linhas por vez. Os cursores são uma extensão dos conjuntos de resultados que fornecem esse mecanismo.

Um cursor é implementado por uma biblioteca de cursores. Esta é um software, normalmente implementado como uma parte do sistema de banco de dados ou uma API de acesso aos dados, utilizada para gerenciar atributos de dados retornados de uma fonte de dados (um conjunto de resultados). Esses atributos incluem gerenciamento simultâneo, posição no conjunto de resultados, número de linhas retornadas e se é possível ou não avançar e/ou voltar no conjunto de resultados (capacidade de navegação).

Um cursor mantém o controle da posição no conjunto de resultados e permite que você execute várias operações, linha por linha em um conjunto de resultados, com ou sem o retorno para a tabela original. Em outras palavras, os cursores, por definição, retornam um conjunto de resultados com base nas tabelas dentro dos bancos de dados. O cursor é então nomeado porque ele indica a posição atual no conjunto de resultados, assim como o cursor em uma tela do computador indica a posição atual.

É importante familiarizar-se com o conceito de cursores antes de seguir adiante para aprender as especificações de seu uso no ADO.

Utilizando os cursores, você pode:

  - Especificar o posicionamento em linhas específicas no conjunto de resultados.

  - Recuperar uma linha ou um bloco de linha com base na posição atual do conjunto de resultados.

  - Modificar dados nas linhas, na posição atual, no conjunto de dados.

  - Definir diferentes níveis de importância para as alterações de dados feitas por outros usuários.

Por exemplo, considere um aplicativo que mostre a um comprador potencial uma lista de produtos disponíveis. O comprador navega pela lista para ver os detalhes e o preço dos produtos e finalmente seleciona um produto para comprar. Navegação e seleção adicionais ocorrem no restante da lista. Para o comprador, os produtos aparecem um por vez, mas o aplicativo usa um cursor de rolagem para navegar para cima e para baixo no conjunto de resultados.

Você pode usar cursores de várias formas:

  - Sem nenhuma linha.

  - Com algumas ou todas as linhas em uma única tabela.

  - Com algumas ou todas as linhas a partir de tabelas unidas de forma lógica.

  - Como somente-leitura ou atualizáveis no nível de cursor ou de campo.

  - Como somente-avançar ou totalmente navegável.

  - Com o conjunto de chaves do cursor localizado no servidor.

  - Importante para as alterações em tabelas subjacentes causadas por outros aplicativos (como associação, classificação, inserções, atualizações e exclusões).

  - Existente no servidor ou no cliente.

Os cursores somente-leitura ajudam os usuários a navegar pelo conjunto de resultados, e os cursores leitura/gravação podem implementar atualizações de linha individuais. Os cursores complexos podem ser definidos com os conjuntos de chaves que apontam de volta para as linhas da tabela de base. Enquanto alguns cursores são somente-leitura em uma direção progressiva, outros podem mover-se para frente e para trás e fornecer uma atualização dinâmica do conjunto de resultados com base nas alterações que outros aplicativos estão fazendo no banco de dados.

Nem todos os aplicativos precisam utilizar cursores para acessar ou atualizar dados. Algumas consultas simplesmente não exigem atualização direta da linha com a utilização do cursor. Os cursores devem ser uma das últimas técnicas escolhidas para a recuperação de dados  em seguida, você deve escolher o cursor com o menor impacto possível. Quando você cria um conjunto de resultados utilizando um procedimento armazenado, o conjunto de resultados não é atualizável com os métodos Edit ou Update do cursor.

## <a name="concurrency"></a>Simultaneidade

Em alguns aplicativos de vários usuários, é extremamente importante que os dados apresentados aos usuários sejam os mais atuais possíveis. Um exemplo clássico de tal sistema é um sistema de reserva de passagens aéreas, em que vários usuários podem estar concorrendo à mesma poltrona em um determinado voo (e, portanto, um único registro). Nesse casso, o design do aplicativo deve lidar com operações simultâneas em um único registro.

Em outros aplicativos, a simultaneidade não é tão importante. Nesses casos, a despesa envolvida em manter os dados sempre atualizados não pode ser justificada.

## <a name="position"></a>Posição

Um cursor também mantém o controle da posição atual em um conjunto de resultados. Pense na posição do cursor como um ponteiro para o registro atual, semelhante ao modo como um índice de matriz aponta para o valor naquele determinado local na matriz.

## <a name="scrollability"></a>Capacidade de navegação

O tipo do cursor utilizado pelo aplicativo também afeta a capacidade de avançar e voltar nas linhas em um conjunto de resultados; isso normalmente é chamado de capacidade de navegação. A capacidade de mover a frente *e* para trás ao longo de um conjunto de resultados aumenta a complexidade do cursor e, portanto, é mais cara implementar. Por essa razão, você deve solicitar um cursor com essa funcionalidade somente quando necessário.

