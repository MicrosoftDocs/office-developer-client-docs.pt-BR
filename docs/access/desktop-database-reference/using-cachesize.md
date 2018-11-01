---
title: Usando CacheSize (referência de banco de dados da área de trabalho do Access)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa624c545d17ef0d56a076b3d30326bacd2c6edf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871959"
---
# <a name="using-cachesize"></a>Uso de CacheSize


**Aplica-se a**: Access 2013, o Office 2013

Use a propriedade **CacheSize** para controlar a quantidade de registros a serem recuperados de uma vez, do provedor para a memória local. Por exemplo, se **CacheSize** for 10, após a abertura inicial do objeto **Recordset**, o provedor irá recuperar os 10 primeiros registros para a memória local. À medida que você se movimentar pelo objeto **Recordset**, o provedor retornará os dados do buffer de memória local. Assim que você passar pelo último registro armazenado em cache, o provedor irá recuperar os 10 registros seguintes da fonte de dados para o cache.


> [!NOTE]
> <P>[!OBSERVAçãO] A propriedade <STRONG>CacheSize</STRONG> baseia-se na propriedade <STRONG>Maximum Open Rows</STRONG> específica do provedor (na coleção <STRONG>Properties</STRONG> do objeto <STRONG>Recordset</STRONG> ). Não é possível definir <STRONG>CacheSize</STRONG> como um valor maior do que <STRONG>Maximum Open Rows</STRONG>. Para modificar o número de linhas que podem ser abertas pelo provedor, defina <STRONG>Maximum Open Rows</STRONG>.</P>



O valor de **CacheSize** pode ser ajustado durante a vida do objeto **Recordset**, mas a alteração desse valor afeta apenas o número de registros do cache após recuperações subsequentes da fonte de dados. Alterar apenas o valor da propriedade não irá alterar o conteúdo atual do cache.

Se o número de registros a serem recuperados for menor do que o especificado em **CacheSize**, o provedor retornará os registros restantes e não ocorrerá erros.

A configuração de **CacheSize** como zero não é permitida e retornará um erro.

Os registros recuperados do cache não refletem as alterações simultâneas feitas por outros usuários na fonte de dados. Para forçar uma atualização de todos os dados armazenados em cache, use o método [Resync](resync-method-ado.md).

Se **CacheSize** for definido como um valor maior do que 1, os métodos de navegação ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext e MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) poderão resultar na navegação para um registro excluído, se a exclusão ocorrer após a recuperação dos registros. Depois da busca inicial, as exclusões subsequentes não serão refletidas no cache de dados, até que você tente acessar um valor de dados de uma linha excluída. No entanto, a definição de **CacheSize** como 1 elimina esse problema, pois as linhas excluídas não podem ser buscadas.

