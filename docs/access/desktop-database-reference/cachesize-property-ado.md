---
title: Propriedade caChesize (ADO)
TOCTitle: CacheSize property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 725c2f81b3f3bce05a3007c50705e9cf35f7008f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296742"
---
# <a name="cachesize-property-ado"></a>Propriedade caChesize (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o número de registros de um objeto [Recordset](recordset-object-ado.md) que ficam armazenados em cache localmente na memória.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que deve ser maior do que 0. O padrão é 1.

## <a name="remarks"></a>Comentários

Use a propriedade **CacheSize** para controlar a quantidade de registros a serem recuperados de uma vez, do provedor para a memória local. Por exemplo, se **CacheSize** for 10, após a abertura inicial do objeto **Recordset**, o provedor irá recuperar os 10 primeiros registros para a memória local. À medida que você se movimentar pelo objeto **Recordset**, o provedor retornará os dados do buffer de memória local. Assim que você passar pelo último registro armazenado em cache, o provedor irá recuperar os 10 registros seguintes da fonte de dados para o cache.

> [!NOTE]
> [!OBSERVAçãO] **CacheSize** baseia-se na propriedade **Maximum Open Rows** específica do provedor (na coleção **Properties** do objeto **Recordset** ). Não é possível definir **CacheSize** para um valor maior do que **Maximum Open Rows**. Para modificar o número de linhas que podem ser abertas pelo provedor, defina **Maximum Open Rows**.

O valor de **CacheSize** pode ser ajustado enquanto o objeto **Recordset** durar, mas a alteração desse valor afetará apenas o número de registros no cache após recuperações subsequentes da fonte de dados. A alteração do valor da propriedade apenas não alterará o conteúdo atual do cache.

Se o número de registros a serem recuperados for menor do que o especificado em **CacheSize**, o provedor retornará os registros restantes e não ocorrerá erros.

Não é permitido definir **CacheSize** como zero e isso provocará um erro.

Os registros recuperados do cache não refletem alterações simultâneas feitas por outros usuários na fonte de dados. Para forçar uma atualização de todos os dados armazenados em cache, use o método [Resync](resync-method-ado.md).

Se **CacheSize** for definida com um valor maior do que um, os métodos de navegação ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext e MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) poderão resultar na navegação para um registro excluído, caso a exclusão ocorra depois que os registros forem recuperados. Após a busca inicial, as exclusões seguintes não serão refletidas no cache de dados até que você tente acessar um valor de dados de uma linha excluída. Contudo, a definição de **CacheSize** como um elimina esse problema, uma vez que as linhas excluídas não poderão ser encontradas.

