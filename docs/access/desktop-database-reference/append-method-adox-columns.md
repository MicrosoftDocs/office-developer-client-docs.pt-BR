---
title: Método Append (Colunas do ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7a6f7ac26c3089a973a68e07acbe0f6f3e4029df
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949436"
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
|*Type* |Opcional. Um valor **Long** que especifica o tipo de dados da coluna. O parâmetro *Type* corresponde à propriedade [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) de um objeto **Column** .|
|*DefinedSize* |Opcional. Um valor **Long** que especifica o tamanho da coluna. O parâmetro *DefinedSize* corresponde à propriedade [DefinedSize](definedsize-property-adox.md) de um objeto **Column** .|


> [!NOTE]
> [!OBSERVAçãO] Ocorrerá um erro ao anexar uma **Coluna** à coleção **Columns** de um [Índice](index-object-adox.md), se a **Coluna** não existir em uma [Tabela](table-object-adox.md) que já esteja anexada à coleção [Tables](tables-collection-adox.md).


