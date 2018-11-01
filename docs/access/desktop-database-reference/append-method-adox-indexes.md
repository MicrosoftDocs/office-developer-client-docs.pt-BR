---
title: Método Append (Índices do ADOX)
TOCTitle: Append Method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b2786de4d1fde2e67e576c2bc81733b1a877a80
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875123"
---
# <a name="append-method-adox-indexes"></a>Método Append (Índices do ADOX)


**Aplica-se a**: Access 2013, o Office 2013



Adiciona um novo objeto [Index](index-object-adox.md) à coleção [Indexes](indexes-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Índices*. Acrescentar*índice* \[,*colunas*\]

## <a name="parameters"></a>Parâmetros

  - *Index*

  - O objeto **Index** a ser anexado ou o nome do índice a ser criado e anexado.

  - *Columns*

  - Opcional. Um valor **Variant** que especifica um ou mais nomes de colunas a serem indexadas. O parâmetro *Columns* corresponde aos valores da propriedade [Name](name-property-adox.md) de um objeto [Column](column-object-adox.md) ou objetos.

## <a name="remarks"></a>Comentários

O parâmetro *Columns* pode levar o nome de uma coluna ou uma matriz de nomes de coluna.

Ocorrerá um erro se o provedor não oferecer suporte para a criação de índices.

