---
title: Coleção Columns (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1827fe11696e28871bdd03594ff0d7057c377dc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720482"
---
# <a name="columns-collection-adox"></a>Coleção Columns (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Contém todos os objetos [Column](column-object-adox.md) de uma tabela, índice ou chave.

## <a name="remarks"></a>Comentários

O método [Append](append-method-adox-columns.md) de uma coleção **Columns** é exclusivo do ADOX. Você pode:

  - Adicionar uma nova coluna à coleção com o método **Append**.

As propriedades e métodos restantes são padrão das coleções do ADO. Você pode:

  - Acessar uma coluna na coleção com a propriedade [Item](item-property-ado.md).

  - Retornar o número de colunas contidas na coleção com a propriedade [Count](count-property-ado.md).

  - Remover uma coluna da coleção com o método [Delete](delete-method-adox-collections.md).

  - Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).


> [!NOTE]
> [!OBSERVAçãO] Ocorrerá um erro ao anexar uma **Coluna** à coleção **Columns** de um [Índice](index-object-adox.md), se a **Coluna** não existir em uma [Tabela](table-object-adox.md) que já esteja anexada à coleção [Tables](tables-collection-adox.md).


