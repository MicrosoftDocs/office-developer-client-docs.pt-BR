---
title: Método Append (Chaves do ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297085"
---
# <a name="append-method-adox-keys"></a>Método Append (Chaves do ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Adiciona um novo objeto [Key](key-object-adox.md) à coleção [Keys](keys-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Chaves*. *Tecla* \[Append,*KeyType* \] \[,*Column* \] \[,*RELATEDTABLE* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Key* |O objeto **Key** a ser anexado ou o nome da chave a ser criada e anexada.|
|*KeyType* |Opcional. Um valor **Long** que especifica o tipo de chave. O parâmetro *Key* corresponde à propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) de um objeto **Key**.|
|*Coluna* |Opcional. Um valor **String** que especifica o nome da coluna a ser indexada. O parâmetro *Columns* corresponde ao valor da propriedade [Name](name-property-adox.md) de um objeto [Column](column-object-adox.md).|
|*RelatedTable* |Opcional. Um valor **String** que especifica o nome da tabela relacionada. O parâmetro *RelatedTable* corresponde ao valor da propriedade **Name** de um objeto [Table](table-object-adox.md).|
|*RelatedColumn* |Opcional. Um valor **String** que especifica o nome da coluna relacionada para uma chave estrangeira. O parâmetro RelatedColumn corresponde ao valor da propriedade **Name** de um objeto **Column**.|

## <a name="remarks"></a>Comentários

O parâmetro *Columns* pode receber o nome de uma coluna ou uma matriz de nomes de colunas.

