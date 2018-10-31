---
title: Método Append (Colunas do ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 727634356a08646b1e2757996cc6bf071de07353
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861572"
---
# <a name="append-method-adox-columns"></a>Método Append (Colunas do ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Adiciona um novo objeto [Column](column-object-adox.md) à coleção [Columns](columns-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Colunas*. Acrescentar*coluna* \[,*tipo* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Parâmetros

  - *Column*

  - O objeto **Column** a ser anexado ou o nome da coluna a ser criada e anexada.

  - *Type*

  - Opcional. Um valor **Long** que especifica o tipo de dados da coluna. O parâmetro *Type* corresponde à propriedade [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) de um objeto **Column** .

  - *DefinedSize*

  - Opcional. Um valor **Long** que especifica o tamanho da coluna. O parâmetro *DefinedSize* corresponde à propriedade [DefinedSize](definedsize-property-adox.md) de um objeto **Column** .


> [!NOTE]
> [!OBSERVAçãO] Ocorrerá um erro ao anexar uma **Coluna** à coleção **Columns** de um [Índice](index-object-adox.md), se a **Coluna** não existir em uma [Tabela](table-object-adox.md) que já esteja anexada à coleção [Tables](tables-collection-adox.md).


