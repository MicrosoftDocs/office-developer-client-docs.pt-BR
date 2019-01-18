---
title: Método Append (Colunas do ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711228"
---
# <a name="append-method-adox-columns"></a>Método Append (Colunas do ADOX)

**Aplica-se a**: Access 2013, o Office 2013

Adiciona um novo objeto [Column](column-object-adox.md) à coleção [Columns](columns-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Colunas*. Acrescentar*coluna* \[,*tipo* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Column* |O objeto **Column** a ser anexado ou o nome da coluna a ser criada e anexada.|
|*Type* |Opcional. Um valor **Long** que especifica o tipo de dados da coluna. O parâmetro *Type* corresponde à propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) de um objeto **Column** .|
|*DefinedSize* |Opcional. Um valor **Long** que especifica o tamanho da coluna. O parâmetro *DefinedSize* corresponde à propriedade [DefinedSize](definedsize-property-adox.md) de um objeto **Column** .|


> [!NOTE]
> [!OBSERVAçãO] Ocorrerá um erro ao anexar uma **Coluna** à coleção **Columns** de um [Índice](index-object-adox.md), se a **Coluna** não existir em uma [Tabela](table-object-adox.md) que já esteja anexada à coleção [Tables](tables-collection-adox.md).


