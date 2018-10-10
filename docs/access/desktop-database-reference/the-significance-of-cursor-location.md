---
title: Significado do local do cursor
TOCTitle: The Significance of Cursor Location
ms:assetid: 57cf91a0-2612-b1ca-1c03-9c1ccb396b2e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249296(v=office.15)
ms:contentKeyID: 48544978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e1b552ac2774fe0c5d47c19924219800e5bdf865
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462829"
---
# <a name="the-significance-of-cursor-location"></a>Significado do local do cursor


**Aplica-se a**: Access 2013 | Office 2013

Todo cursor usa recursos temporários para manter seus dados. Esses recursos podem ser a memória, um arquivo de paginação de disco, arquivos de disco temporários ou mesmo repositório temporário no banco de dados. O cursor é chamado um cursor *do cliente* quando esses recursos estão localizados no computador cliente. O cursor é chamado um cursor do *lado do servidor* quando esses recursos estão localizados no servidor.

## <a name="client-side-cursors"></a>Cursores do lado do cliente

No ADO, chame um cursor do lado do cliente usando **adUseClient** **CursorLocationEnum**. Com um cursor do lado do cliente que não seja de conjunto de chaves, o servidor envia o conjunto de resultados inteiro para o computador cliente, através da rede. O computador cliente fornece e gerencia os recursos temporários necessários para o cursor e o conjunto de resultados. O aplicativo do lado do cliente pode navegar no conjunto de resultados inteiro para determinar quais são as linhas necessárias.

Os cursores do lado do cliente, estáticos e controlados por conjuntos de chaves, podem representar uma carga significativa para a estação de trabalho, caso incluam linhas em excesso. Embora todas as bibliotecas de cursores sejam capazes de criar cursores com milhares de linhas, os aplicativos desenvolvidos para buscar esses grandes conjuntos de linhas podem apresentar um desempenho insatisfatório. Há exceções, é claro. Para alguns aplicativos, um cursor grande do lado do cliente pode ser perfeitamente adequado e o desempenho pode não ser um problema.

Um benefício óbvio do cursor do lado do cliente é a resposta rápida. Após o conjunto de resultados ser baixado no computador cliente, a navegação pelas linhas é muito rápida. O aplicativo em geral é mais escalonável com os cursores do lado do cliente, pois as necessidades de recursos do cursor são colocadas separadamente em cada cliente, e não no servidor.

## <a name="server-side-cursors"></a>Cursores do servidor

No ADO, chame um cursor do servidor usando **adUseServer** **CursorLocationEnum**. Com esse cursor, o servidor gerencia o conjunto de resultados usando recursos fornecidos pelo computador servidor. O cursor do servidor retorna através da rede apenas os dados solicitados. Esse tipo de cursor às vezes pode oferecer um desempenho melhor do que o cursor do lado do cliente, especialmente em situações nas quais o tráfego excessivo da rede é um problema.

No entanto, é importante observar que um cursor do servidor está  pelo menos temporariamente  consumindo recursos preciosos do servidor para cada cliente ativo. É necessário planejamento para garantir que o hardware do servidor consiga gerenciar todos os cursores do servidor solicitados pelos clientes ativos. Além disso, esse cursor pode ser lento, pois fornece apenas acesso a linha única  não há cursor em lote disponível.

Os cursores do servidor são úteis para inclusão, atualização ou exclusão de registros. Com eles, é possível ter várias instruções ativas na mesma conexão.
