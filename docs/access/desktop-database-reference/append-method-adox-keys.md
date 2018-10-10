---
title: Método Append (Chaves do ADOX)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7e10e272155d2d0377810bf8aa1704a30bad39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464856"
---
# <a name="append-method-adox-keys"></a>Método Append (Chaves do ADOX)


**Aplica-se a**: Access 2013 | Office 2013


Adiciona um novo objeto [Key](key-object-adox.md) à coleção [Keys](keys-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Chaves*. Acrescentar*chave* \[,*KeyType* \] \[,*coluna* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Parâmetros

  - *Key*

  - O objeto **Key** a ser anexado ou o nome da chave a ser criada e anexada.

  - *KeyType*

  - Opcional. Um valor **Long** que especifica o tipo de chave. O parâmetro *Key* corresponde à propriedade [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) de um objeto **Key** .

  - *Column*

  - Opcional. Um valor **String** que especifica o nome da coluna a ser indexada. O parâmetro *Columns* corresponde ao valor da propriedade [Name](name-property-adox.md) de um objeto [Column](column-object-adox.md) .

  - *RelatedTable*

  - Opcional. Um valor **String** que especifica o nome da tabela relacionada. O parâmetro *RelatedTable* corresponde ao valor da propriedade **Name** de um objeto [Table](table-object-adox.md) .

  - *RelatedColumn*

  - Opcional. Um valor **String** que especifica o nome da coluna relacionada para uma chave estrangeira. O parâmetro RelatedColumn corresponde ao valor da propriedade **Name** de um objeto **Column**.

## <a name="remarks"></a>Comentários

O parâmetro *Columns* pode levar o nome de uma coluna ou uma matriz de nomes de coluna.
